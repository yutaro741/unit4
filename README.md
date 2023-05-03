# Unit 4: Math project

## Criteria A: Planning
**Problem defenition**

Cliant M is a student studying in high school. He is a math enthusiast to the point of enthusiasm, solving difficult math problems and making new math theorems on a daily life. He wants a place on the Internet where he can share his mathematical theorems, problems, and solutions. In the Network, he requires the Login and Register system for using his own account. And he requested to be able to post text and pictures for showing some graphs/fiugre. Also, he strongly requested to be able to use some math text type(ex;Latex, Katex, ...), to make it easy to visuallise. Additionally, he reqires to be able to send some personal message to onother account, for error reporting and collaborative research.

**Proposed Solution**

Design Statement to solve my client's problem, I will create an application to post the information about math. I will be using Python as the primary programing launguage for the application, HTML and CSS for the graphical user interface(GUI), and SQLite to manipulate the database in which the post and account logs will be stored. The application will consist a login page, registration page, main page, post page, edit page and chat page.

System The application to manage appliance usage will be developed on the programming editor PyCharm version 2022.3.2, run on a 2020 MacBook Pro using the OS macOS Big Sur version 13.2.1. Through PyCharm, the application will be coded using Python, HTML and CSS for the GUI, and SQLite to manipulate the database.

**Design statement**

Software Justification
Python

Python is an ideal programming language for this application due to its versatility, especially when it comes to handling data and working with databases. The use of Python will also allow for the integration of math text types such as Latex and Katex, which will be essential for visualizing mathematical formulas and theorems. Additionally, Python's robust library support will make it possible to implement the necessary features for the login, registration, messaging, and posting functionality efficiently. Therefore, Python is the ideal choice for this project due to its flexibility, simplicity, and efficient development capabilities.


HTML and CSS

HTML and CSS are essential for creating the graphical user interface (GUI) of the application, allowing the client to interact with the system and post mathematical theorems, problems, and solutions. HTML is used to create the structure and content of web pages, while CSS is used to style and format them. Additionally, HTML can be used to incorporate math text types like Latex and Katex, as requested by the client, which will make it easy for the client to visualize mathematical expressions.


SQLite

SQLite is an ideal choice for this application as it provides a lightweight, self-contained, and efficient database management system that can handle the data storage and retrieval needs of this application. Additionally, SQLite offers excellent compatibility with Python, which I am gonna use for this application. Overall, SQLite's reliability, efficiency, and compatibility make it an excellent choice for managing the database in this math-sharing application.



**Success Criteria**

1. Make Login system and Register system (Encrypt password)
2. Make Adding posts(title, content, account) system.
3. Able to use Tex font style for the post.
4. Able to comment to the post.
5. Make posts editing system.
6. Able to do the private chat between multiple accounts.


## Criteria B: Design
**System Diagram**

**UML Diagram**

**ER diagram**

**Flow Diagrams**

**Record of Tasks**

**Test plan**

## Criteria C: Coding##
Python:p, HTML/CSS:H, SQL:Q other ideas: O

1. H: link rel to connect to CSS from HTML.
I made the pass from HTML to CSS to be able to use the coding in CSS to HTML. I will use the same CSS for all pages. I will use this for all of the HTML pages, to aboid writting all of the CSS every time. 
```.py
<link rel="stylesheet" href="../static/my_style.css">
```


2. H: input, button, form
This is the form to write the information from user, such as username and password. I wrote as method=POST that I can use after in python.
```.py
<main>
    <div class="row">
        <div class="colm-form">
            <div class="form-container">
                <form method="POST">
                    <input type="text" name="username" placeholder="username">
                    <input type="password" name="password" placeholder="Password">
                    <button class="btn-login">Login</button>
                </form>
            </div>
            <p><a href="#"><b>Login to `PostMath`</b></a> to the new math world.</p>
        </div>
    </div>
</main>
 ```
3. H: CSS writting(background-color, border, padding, color)
Because I wrote the class that I didn't make so far, I need to make those. I made class called, row, colm-form, form-container, btn-login. By making writing a CSS code for login system, I used background-color, border, padding, color and many other way. This is one of example.
```.py
.colm-form .form-container .btn-login {
    background-color: #1877f2;
    border: none;
    border-radius: 6px;
    font-size: 20px;
    padding: 0 16px;
    color: #ffffff;
    font-weight: 700;
}
```

4. P: Flask, function, render_template
To run the function, I will use Python-flask. I will use .route method and render template to show the HTML file page.
```.py
from flask import Flask, render_template, request, redirect, url_for, make_response
app = Flask(__name__)
app.route("/login")
def login():
    return render_template("login.html")
if __name__ == '__main__':
    app.run()
```

Now, I can run the code to see the HTML and able to develop while I am looking things that I made.


5. P: If statement, methods(get and post) method, request method.
I wanna get the text that user inputed into HTML file. To get those data, I will use request method of Flask. Also, I use methods(get, post) method to get the bool that the Login button is pressed or not. method=post is writting in the HTML code. The code below is the code to get the username and password from the GUI when button is clicked.
```.py
@app.route("/login", methods=["GET", "POST"])
def login():
    if request.method == "POST":
        username = request.form["username"]
        password = request.form["password"]
```

6. Q: SELECT, P: Cookies, class
As I got the information from the user, I want to check that username and password is exist in the database. I reuse the code from "unit3", class database_handler. Please look at repositly of unit3project if you want to use this code. (the database is already created with using the CREATE TABLE statement(P/Q). 
So, I use SELECT method to get the data of user that has same username. Than, I checked password of that user that is hashed.
Also, I need to save the information that user is logined. So, I use cookies (from Flask) to save the user_id to the cookies.
```.py
from my_lib import database_handler

@app.route("/login", methods=["GET", "POST"])
def login():
    if request.method == "POST":
        username = request.form["username"]
        password = request.form["password"]
        if len(username) > 0 and len(password) > 0:
            db = database_handler()
            user = db.get_info(f"""SELECT * FROM users WHERE username='{username}'""")
            if user:
                user = user[0]
                id, username, hashed = user
                if database_handler().hash(password) == hashed:
                    print("password is correct")
                    resp = make_response(redirect(url_for("get_user", userid=id)))
                    resp.set_cookie("user_id", f"{id}")
                    return resp
    user_id = 0
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")
    return render_template("login.html", user_id=user_id)
```

Now, my login system is done. 

7. O: Re_check password system, Q:INSERT.
I made the login system, but I don't have my account yet. So, I will make the registeration system. Fortunetly, it is almost same thing, so I will not write about dtails. The things we do different is to make the re_check of the password in the HTML and python, and INSERT system to add the data to the database:users.
```.py
......

if password != password_check:
    message = "Password don't match or too short"
else:
    db = database_handler()
    existing_user = db.get_info(f"""SELECT * from USERS where username='{username}'""")
    if existing_user:
        message = "user with that username is exist."
    else:
        new_user = f"""INSERT into users(username, password) values('{username}', '{db.hash(password)}')"""
        db.run_query(new_user)
        message = "registration success!"
        db.close()
......
```

7.5. O: Logout
I made the system to logout. It is just reset the cookies, but somehow reset cookies don't work, so I set the cookies for 0 seconds, means reset the cookies.
```.py
@app.route("/logout")
def logout():
    resp = make_response(redirect(url_for("main")))
    resp.set_cookie('user_id', "", max_age=0)
    return resp
```

8: H/P: jinja2(for loop), template_enjine
The main page needs to be able to see all posts, but it is hard to show all of those posts at once with using only normal HTML. So, I use jinja2 for using for loop for all data, and template_enjine(the things that is in the {{}}) to show each item from python.

※The python file is already made, made by just SELECT all of the posts.
```.py
<h1>table of posts</h1>
<table style="border-collapse:collapse">
    <tr>
        <th class="num">user_id</th>
        <th>author</th>
        <th>title</th>
    </tr>
    {% for i in posts %}
        <tr>
            <th><a href="{{ url_for('get_user', userid=i[1]) }}">{{ i[1] }}</a></th>
            <th><a href="{{ url_for('get_user', userid=i[1]) }}">{{ i[4] }}</a></th>
            <th><a href="{{ url_for('post', post_id=i[0]) }}">{{ i[2] }}</a></th>
        </tr>
    {% endfor %}
</table>
```
Main page is done!!

9: H/O: MathJax
Finally, I am able to show the data from the database, However, that data that we can see is just a text. i want to see the text, with using the Tex font style. I use MathJax to show all of those things. 
```.py
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
    ......
</head>
<body onload="MathJax.typeset()">
...
```
