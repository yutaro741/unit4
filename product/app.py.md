This is the code for python program, named app.py

```.py
from flask import Flask, render_template, request, redirect, url_for, make_response
from my_lib import database_handler

app = Flask(__name__)

@app.route("/user/<userid>", methods=['GET', 'POST'])#Get user id for the input value. Also it shows inside the link.
def get_user(userid):
    if request.cookies.get('user_id'):#If user is logined, keep going. If not, go to login screen.
        user_id = request.cookies.get("user_id")
        user_id = int(user_id)
    else:
        return redirect(url_for('login'))
    db = database_handler()
    if request.method == "POST": #if save button is pressed:
        if str(userid) == str(user_id):#Check the button that post button is clicked or message button is pressed.
            title = request.form['title']
            content = request.form['content']
            if len(title) > 0 and len(content) > 0:#Filter not to post Null posts.
                new_post = f"""INSERT into posts(title, content, user_id) values('{title}', '{content}', {user_id})"""
                db.run_query(new_post)
                return redirect(url_for("get_user", userid=userid))
        else:#Code that message button is clicked
            content = request.form['message']
            query = f"""INSERT into chats(me_id, you_id, content) values({user_id},{userid},'{content}')"""
            db.run_query(query)
            return redirect(url_for("get_user", userid=userid))

    #Code below is for getting all of the messages.
    query = f"""SELECT * from chats WHERE (me_id = {userid} and you_id = {user_id}) or (me_id = {user_id} and you_id = {userid}) ORDER BY id DESC"""
    chat = db.get_info(query)#Get all of the messages that logined user sent/recieved
    out = []
    for i in chat:#Add each username into the message list.
        s = [i[0], i[1], i[2], i[3]]
        query = f"""SELECT username from users WHERE id={i[1]}"""
        x = db.get_info(query)
        s.append(x[0][0])
        query = f"""SELECT username from users WHERE id={i[2]}"""
        x = db.get_info(query)
        s.append(x[0][0])
        out.append(s)
    chats = db.get_chat(user_id)

    posts, user = None, None#Find out all of the posts that selected user wrote.
    user = db.get_info(f"""SELECT * from users where id={userid}""")
    requested_user = user[0]
    if user:#存在するか。(Noneでないか)覚えておこう。
        posts = db.get_info(f"""SELECT * from posts where user_id={userid} ORDER BY id DESC""")
    db.close()
    return render_template("profile.html", user=requested_user, posts=posts, me=int(user_id), user_id=requested_user[0], chat=out, chats=chats)

@app.route("/registeration",methods=["GET","POST"])
def registration():
    message = ""
    if request.method == "POST":#Code if the button is clicked.
        username = request.form["username"]
        password = request.form["password"]
        password_check = request.form["password_check"]
        if password != password_check:#Check if password and password check is same
            message = "Password don't match or too short"
        else:
            db = database_handler()#Check if there is same username exist.
            existing_user = db.get_info(f"""SELECT * from users where username='{username}'""")
            if existing_user:
                message = "user with that username is exist."
            else:#Hash password, save into database, get user id, save user id to cookie, go to profile page.
                new_user = f"""INSERT into users(username, password) values('{username}', '{db.hash(password)}')"""
                db.run_query(new_user)
                id = db.get_info(f"""SELECT id from users where username='{username}'""")
                id = id[0][0]
                db.close()
                resp = make_response(redirect(url_for("get_user", userid=id)))
                resp.set_cookie("user_id", f"{id}")
                return resp
    user_id = 0#The program that is coded for all of the pages.
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")
    return render_template("registration.html", message=message, user_id=user_id)

@app.route("/login", methods=["GET", "POST"])
def login():
    if request.method == "POST":#Check if the button is clicked.
        username = request.form["username"]
        password = request.form["password"]
        if len(username) > 0 and len(password) > 0:#check the entered password is not null.
            db = database_handler()
            user = db.get_info(f"""SELECT * FROM users WHERE username='{username}'""")
            if user:#Check there is account with same username
                user = user[0]
                id, username, hashed = user
                if database_handler().hash(password) == hashed:#Check that account's password is same as entered password.
                    print("password is correct")
                    resp = make_response(redirect(url_for("get_user", userid=id)))
                    resp.set_cookie("user_id", f"{id}")#save user id to cookies and go to profile page.
                    return resp
    user_id = 0#The program that is for all pages.
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")
    return render_template("login.html", user_id=user_id)

@app.route("/logout")
def logout():#It seems like a page, but it is just going to main page after cookie expired.
    resp = make_response(redirect(url_for("main")))
    resp.set_cookie('user_id', "", max_age=0)
    return resp

@app.route("/main")
def main():
    db = database_handler()#First get all of the posts.
    posts = db.get_info(f"""SELECT * from posts ORDER BY id DESC""")
    out = []
    for i in posts:#Add username of the writer.
        s = [i[0], i[1], i[2], i[3]]
        u_name = db.get_info(f"""SELECT username from users where id={i[1]}""")
        u_name = u_name[0][0]
        s.append(u_name)
        out.append(s)
    user_id = 0#This is the program that is in all pages for header.
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")
    chats = db.get_chat(user_id)#Here is to find the all of the posts.
    query = f"""SELECT id, username from users WHERE id IN (SELECT DISTINCT user_id from posts)"""
    all_users = db.get_info(query)
    db.close()
    return render_template("main.html", posts=out, all_users=all_users, user_id=user_id, chats=chats)

@app.route("/post/<post_id>",  methods=['GET', 'POST'])
def post(post_id):
    db = database_handler()
    data = db.get_info(f"""SELECT * from posts WHERE id={post_id}""")
    if not request.cookies.get("post_id"):#Save the post id into cookie.
        resp = make_response(redirect(url_for("post", post_id=post_id)))
        resp.set_cookie('post_id', f"{post_id}")
        return resp

    data = data[0]
    is_user = False
    if request.cookies.get('user_id'):#Get user id and compare with post id.
        user_id = request.cookies.get("user_id")
        if int(user_id) == data[1]:
            is_user = True

    if request.method == "POST":#If the button is clicked:
        post_id = 0
        if request.cookies.get('post_id'):
            post_id = int(request.cookies.get("post_id"))
        title = request.form['title']
        content = request.form['content']
        if len(title)>0 and len(content)>0:#Check if the inputed title and content is not null
            query = f"""UPDATE posts SET title='{title}', content='{content}' WHERE id={post_id}"""
            db.run_query(query)
        db.close()
        return redirect(url_for("main"))#Go to main page after the post.
    db.close()

    user_id = 0#This is the code for header, and it just take user id from cookies and go back.
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")

    return render_template("post.html", data=data, is_user=is_user, user_id=user_id)

if __name__ == '__main__':
    app.run()#run the program here.

```
