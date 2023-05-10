# Unit 4: Math project
![](https://github.com/yutaro741/unit4/blob/main/pictures/craiyon_201247_There_is_pen_at_the_middle_of_the_picture__and_many_math_formula_around_it_.png)
[^1]

[figure 1] AI generated figure 
[^1]:Craiyon, AI Image Generator, https://www.craiyon.com/. Accessed 7 May 2023.

## Criteria A: Planning
**Problem defenition**

Client M is a student studying in high school. He is a math enthusiast to the point of enthusiasm, solving difficult math problems and making new math theorems on a daily life. He wants a place on the Internet where he can share his mathematical theorems, questions, and answers. He wants not only share his own math work, but want to see the posts that people made. He tries to find those kind of website, and finds "hatenablog" or "Quora". However, those alternative website don't matches to his wants, and hard to communicate privatly, or hard to post the math formulas.

So, he asks me to make new website. In the website, he requires the Login system for using and be able to use personal account to manage math posts. Also, he strongly requested to be able to use text font of math, to make it easy to visuallise. In detail, he requires to use Latex(or any other Tex style), because that is the things that is most familiar with him, and also it is the one of the most famous math display system in the world. Additionally, he wants to interact and communicate the people that makes the interesting posts. (Evidence of consulation[^2], [^3])

[^2]:https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-07%20at%2018.12.09.png
[^3]:https://docs.google.com/document/d/1Kb-PJmdfSfLfV1fQcWi3mHb1rIDEvV2lEOeDdsIuNFg/edit?usp=sharing

**Success Criteria**

1. [issue tackled: To be able to use personal account to manage math posts for each user.] The user can register, login and logout of the system.
2. [issue tackled: For getting the requirements, login, register, post at the same time. Doing all of the requirements at the same page is unnecessary and difficult to use. Therefore, we needs to make multiple pages, and system to move those pages.]The user can switch between different pages.
3. [issue tackled: To solve the core parts of his wants, manage his post]The system can add and edit posts, including information on title, content, and account.
4. [issue tackled: his wants. Tex style]The system is able to show all text with Tex font style.
5. [issue tackled: the wants of his creation with No3]The user can view all posts that are made by all users.
6. [issue tackled: For interacting and communicating with each people, chat system is the most appropriate.]The user can do the private chat between other accounts.

The confirmation from cliant
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-07%20at%2020.25.54.png)

**Proposed Solution**

Design Statement to solve my client's problem, I will create an application to post the information about math. I will be using Python as the primary programing launguage for the application, HTML and CSS for the graphical user interface(GUI), and SQLite to manipulate the database in which the post and account logs will be stored. The application will consist a login page, registration page, main page, post page, edit page and chat page.

System The application to manage appliance usage will be developed on the programming editor PyCharm version 2022.3.2, run on a 2020 MacBook Pro using the OS macOS Big Sur version 13.2.1. Through PyCharm, the application will be coded using Python, HTML and CSS for the GUI, and SQLite to manipulate the database.

**Design statement**

## Rational for the proposed solution

**Why a website?**
Websites can be accessed simply by opening a browser, making them easier to use than applications. Websites can also be accessed from a variety of devices, so they can be used from mobile devices, tablets, and others. Also, website, collaboration among users is facilitated. For example, success criteria No6, I need to be able to make a chat system. Using website is more beneficial and useful than other systems(eg:system belongs to download).

**Why Python?**[^4]
Python is an ideal programming language for this application due to its versatility, especially when it comes to handling data and working with databases. The use of Python will also allow for the integration of math text types such as Latex and Katex, which will be essential for visualizing mathematical formulas and theorems. Additionally, Python's robust library support will make it possible to implement the necessary features for the login, registration, messaging, and posting functionality efficiently. I had other choises of programming launguages, such as JavaScript[^5], but integration with web frameworks like Flask, and scientific computing libraries like NumPy, SciPy, and Matplotlib was　Superior than Javascript. Also, I can use Javascript by putting the code in the HTML file, but using python while using javascript as a main programming launguage is not efficient. Therefore, python is the best programming launguage for doing this project.

[^4]:“Applications for Python.” Python.org, https://www.python.org/about/apps/#web-and-internet-development. 
[^5]:Learn JavaScript Online - Courses for Beginners - javascript.com, https://www.javascript.com/.

**Why Flask?**[^5]
Flask is a lightweight web framework in Python that is particularly well-suited for building small to medium-sized web applications. Flask is an ideal choice for this project for several reasons. Flask is lightweight and simple, making it an excellent choice for small projects, such as the math posting and sharing system that I am trying to make. Also, the flask has the ability to connect the python and sqlite to HTML, that I am gonna use for this project. Here, Flask is used to load file from multiple files. Additionally, Flask has an minimalistic framework, meaning that it doesn't come with as many built-in features compared with onother system, such as Django. While this might seem like a disadvantage, it can actually be an advantage for projects where I don't need all of the features that Django offers.

[^5]:Welcome to Flask — Flask Documentation (2.3.x), https://flask.palletsprojects.com/en/2.3.x/.

**Why SQLite?**[^6]
SQLite is an ideal choice for this application as it provides a lightweight, self-contained, and efficient database management system that can handle the data storage and retrieval needs of this application. Additionally, SQLite offers excellent compatibility with Python, which I am gonna use for this application. Also, SQLite is a serverless database management system, meaning that it doesn't require a separate server process to operate. This can simplify deployment and maintenance, as there is no need to set up and maintain a separate server process. Finally, the uses of 'new line' that happens if user wants to make a long posts, I am struggled to determine was best fit compared with other database management systems. Overall, SQLite's reliability, efficiency, and compatibility make it an excellent choice for managing the database in this application.
[^6]:https://sqlite.org/index.html
[^7]:https://cloudinfrastructureservices.co.uk/sqlite-vs-sql-whats-the-difference/#:~:text=SQLite%20vs%20SQL%20(Comparison),used%20to%20access%20the%20database.


## Criteria B: Design
**System Diagram**

**UML Diagram**

**ER diagram**

Examples of ER diagram:
users
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.32.png)
posts
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.43.png)
chats
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.49.png)

**Flow Diagrams**

**Record of Tasks**
| Task No 	| task                                               	| Planned Outcome                                                                                                                                      	| Time estimate 	| Target completion date 	| Criterion 	|
|---------	|----------------------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------	|---------------	|------------------------	|-----------	|
|       1 	| First meeting with client                          	| Identify problem, set up future meeting(s)                                                                                                           	| 20m           	|                  Feb20 	| A         	|
|       2 	| Write success criteria                             	| Write proposed solution and success criteria.                                                                                                        	| 20m           	|                  Feb20 	| A         	|
|       3 	| Get apploval from cliants                          	| Send email and get approval.                                                                                                                         	| 3m            	|                  Feb20 	| A         	|
|       4 	| Research rationale                                 	| Research and create a logical rationale behind the tools used for the proposed solution                                                              	| 1h            	|                  Feb20 	| B         	|
|       5 	| Create login page                                  	| Program the kivymd and python files for the GUI and functionality of the login page                                                                  	| 40min         	|                  Feb20 	| C         	|
|       6 	| Create registration page                           	| Program the kivymd and python files for the GUI and functionality of the registration page                                                           	| 40min         	|                  Feb20 	| C         	|
|       7 	| Create Main page                                   	| Program the kivymd and python files for the GUI and functionality of the main page                                                                   	| 1h            	|                  Feb20 	| C         	|
|       8 	| Create page to add note                            	| Program the kivymd and python files for the GUI and functionality of the note add page                                                               	| 1h            	|                  Feb20 	| C         	|
|       9 	| Create page to edit note                           	| Program the kivymd and python files for the GUI and functionality of the note edit page                                                              	| 30m           	|                  Feb20 	| C         	|
|      10 	| Create system to get color                         	| Program the python file for functionality to get the color with color code and some of color with str.(eg:red, green, purple, white, b, Orange, ...) 	| 4h            	|                  Feb20 	| C         	|
|      11 	| Create system to find complementary color          	| Program the python function to find complementary color and apply to text.                                                                           	| 1h            	|                  Feb20 	| C         	|
|      12 	| Create 80 buttons for substitution of MDDataTable. 	| Program the kivymd and python files for the GUI and functionality to see the all tasks in main page. I can't use MDDatatable.                        	| 5h            	|                  Feb20 	| C         	|
|      13 	| Let buttons able to change colors                  	| Let button to be able to change background color and text color                                                                                      	| 20m           	|                  Feb20 	| C         	|
|      14 	| Make the GUI it bit clean                          	| Program the kivymd for GUI able to see a bit better way.                                                                                             	| 10m           	|                  Feb20 	| C         	|
|      15 	| Second meeting with cliant                         	| Let cliant see the prototype and get approval.                                                                                                       	| 10m           	|                  Feb27 	| A         	|
|      16 	| Be able to use MDColorPicker and  MDDatePicker     	| Ask to ChatGPT, and install something strange to be able to use all of the program.                                                                  	| 5m            	|                  Feb27 	| N/A       	|
|      17 	| Delete everything                                  	| Delete all of the data that I made in Kivymd and Python                                                                                              	| 20sec         	|                  Feb27 	| N/A       	|
|      18 	| Code MDDataTable                                   	| Code MDDataTable and test it is really able to use it or not.                                                                                        	| 30m           	|                  Feb27 	| C         	|
|      19 	| Create login page                                  	| Program the kivymd and python files for the GUI and functionality of the login page                                                                  	| 20m           	|                  Feb27 	| C         	|
|      20 	| Create registration page                           	| Program the kivymd and python files for the GUI and functionality of the registration page                                                           	| 10m           	|                  Feb27 	| C         	|
|      21 	| Create Main page                                   	| Program the kivymd and python files for the GUI and functionality of the main page                                                                   	| 2h            	|                  Feb27 	| C         	|
|      22 	| Test check box                                     	| Try to make a check box for the category selection                                                                                                   	| 30m           	|                  Feb27 	| C         	|
|      23 	| Create page to add note                            	| Program the kivymd and python files for the GUI and functionality of the note add page                                                               	| 1h            	|                  Feb27 	| C         	|
|      24 	| Create page to edit note                           	| Program the kivymd and python files for the GUI and functionality of the note edit page                                                              	| 30m           	|                  Feb27 	| C         	|
|      25 	| Create page to see all tasks with MDDataTable      	| Program the kivymd and python files for the GUI and functionality of to see all of the data using MDDataTable                                        	| 1.5h          	|                   Mar3 	| C         	|
|      26 	| Let MDDataTable directly move to Editingscreen     	| Program python that can directry move to Editingscreen if I press one of task shown.                                                                 	| 40min         	|                   Mar3 	| C         	|
|      27 	| Let able to delete tasks in data table             	| Program python file that I can directry delete my tasks that I select in checkbox.                                                                   	| 20min         	|                   Mar3 	| C         	|
|      28 	| Let able to change color in Data table.            	| Program python file that each tasks is colored with choosen color                                                                                    	| 30min         	|                   Mar3 	| C         	|
|      29 	| Create MDColorPicker                               	| Program the kivymd and python files for the GUI and functionality to select color easelly.                                                           	| 1h            	|                   Mar3 	| C         	|
|      30 	| Create MDdatepicker                                	| Program the kivymd and python files for the GUI and functionality to select date easelly.                                                            	| 30m           	|                   Mar3 	| C         	|
|      31 	| Create MDCheckbox                                  	| Program the kivymd and python files for the GUI and functionality to select category easelly.                                                        	| 1h            	|                   Mar3 	| C         	|
|      32 	| Apply those to add page                            	| let MDColorPicker, MDDatepicker, MDCheckbox use in add page.                                                                                         	| 30m           	|                   Mar3 	| C         	|
|      33 	| Write Proposed Solution                            	| Write proposed solution.                                                                                                                             	| 2h            	|                   Mar3 	| A         	|
|      34 	| Apply those to edit page                           	| let MDColorPicker, MDDatepicker, MDCheckbox use in edit page.                                                                                        	| 40m           	|                   Mar3 	| C         	|
|      35 	| Third meeting with cliant                          	| Let cliant see the prototype and get approval.                                                                                                       	| 15m           	|                   Mar3 	| A         	|
|      36 	| Write UML diagram                                  	| Draw UML diagram with my PC.                                                                                                                         	| 40m           	|                   Mar8 	| B         	|
|      37 	| Write wireframe diagram                            	| Draw wireflame with whitebord                                                                                                                        	| 20m           	|                   Mar8 	| B         	|
|      38 	| Write System diagram                               	| Draw sustem diagram with my PC.                                                                                                                      	| 40m           	|                   Mar8 	| B         	|
|      39 	| Write flow diagrams                                	| Draw flow diagrams with whitebord                                                                                                                    	| 1h            	|                   Mar8 	| B         	|
|      40 	| Put the comment of the python code                 	| Write explanation and comments of the code in python.                                                                                                	| 1.5h          	|                   Mar8 	| C         	|
|      41 	| Make the code clean                                	| Make kivy for GUI to make more clean and organised.                                                                                                  	| 30m           	|                   Mar8 	| C         	|
|      42 	| Take a video.                                      	| Take a demonstration video.                                                                                                                          	| 20m           	|                   Mar8 	| D         	|
|      43 	| Edit a video                                       	| Edit a demonstration video                                                                                                                           	| 40m           	|                   Mar8 	| D         	|
|      44 	| Remake system diagrams                             	| Draw system diagram with the color                                                                                                                   	| 1h            	|                  Mar10 	| B         	


**Test plan**



| Task No 	| task                                               	| Planned Outcome                                                                                                                                      	| Time estimate 	| Target completion date 	| Criterion 	|
|---------	|----------------------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------	|---------------	|------------------------	|-----------	|
|       1 	| First meeting with client                          	| Identify problem, set up future meeting(s)                                                                                                           	| 20m           	|                  Feb20 	| A         	|
|       2 	| Write success criteria                             	| Write proposed solution and success criteria.                                                                                                        	| 20m           	|                  Feb20 	| A         	|
|       3 	| Get apploval from cliants                          	| Send email and get approval.                                                                                                                         	| 3m            	|                  Feb20 	| A         	|
|       4 	| Research rationale                                 	| Research and create a logical rationale behind the tools used for the proposed solution                                                              	| 1h            	|                  Feb20 	| B         	|
|       5 	| Create login page                                  	| Program the kivymd and python files for the GUI and functionality of the login page                                                                  	| 40min         	|                  Feb20 	| C         	|
|       6 	| Create registration page                           	| Program the kivymd and python files for the GUI and functionality of the registration page                                                           	| 40min         	|                  Feb20 	| C         	|
|       7 	| Create Main page                                   	| Program the kivymd and python files for the GUI and functionality of the main page                                                                   	| 1h            	|                  Feb20 	| C         	|
|       8 	| Create page to add note                            	| Program the kivymd and python files for the GUI and functionality of the note add page                                                               	| 1h            	|                  Feb20 	| C         	|
|       9 	| Create page to edit note                           	| Program the kivymd and python files for the GUI and functionality of the note edit page                                                              	| 30m           	|                  Feb20 	| C         	|
|      10 	| Create system to get color                         	| Program the python file for functionality to get the color with color code and some of color with str.(eg:red, green, purple, white, b, Orange, ...) 	| 4h            	|                  Feb20 	| C         	|
|      11 	| Create system to find complementary color          	| Program the python function to find complementary color and apply to text.                                                                           	| 1h            	|                  Feb20 	| C         	|
|      12 	| Create 80 buttons for substitution of MDDataTable. 	| Program the kivymd and python files for the GUI and functionality to see the all tasks in main page. I can't use MDDatatable.                        	| 5h            	|                  Feb20 	| C         	|
|      13 	| Let buttons able to change colors                  	| Let button to be able to change background color and text color                                                                                      	| 20m           	|                  Feb20 	| C         	|
|      14 	| Make the GUI it bit clean                          	| Program the kivymd for GUI able to see a bit better way.                                                                                             	| 10m           	|                  Feb20 	| C         	|
|      15 	| Second meeting with cliant                         	| Let cliant see the prototype and get approval.                                                                                                       	| 10m           	|                  Feb27 	| A         	|
|      16 	| Be able to use MDColorPicker and  MDDatePicker     	| Ask to ChatGPT, and install something strange to be able to use all of the program.                                                                  	| 5m            	|                  Feb27 	| N/A       	|
|      17 	| Delete everything                                  	| Delete all of the data that I made in Kivymd and Python                                                                                              	| 20sec         	|                  Feb27 	| N/A       	|
|      18 	| Code MDDataTable                                   	| Code MDDataTable and test it is really able to use it or not.                                                                                        	| 30m           	|                  Feb27 	| C         	|
|      19 	| Create login page                                  	| Program the kivymd and python files for the GUI and functionality of the login page                                                                  	| 20m           	|                  Feb27 	| C         	|
|      20 	| Create registration page                           	| Program the kivymd and python files for the GUI and functionality of the registration page                                                           	| 10m           	|                  Feb27 	| C         	|
|      21 	| Create Main page                                   	| Program the kivymd and python files for the GUI and functionality of the main page                                                                   	| 2h            	|                  Feb27 	| C         	|
|      22 	| Test check box                                     	| Try to make a check box for the category selection                                                                                                   	| 30m           	|                  Feb27 	| C         	|
|      23 	| Create page to add note                            	| Program the kivymd and python files for the GUI and functionality of the note add page                                                               	| 1h            	|                  Feb27 	| C         	|
|      24 	| Create page to edit note                           	| Program the kivymd and python files for the GUI and functionality of the note edit page                                                              	| 30m           	|                  Feb27 	| C         	|
|      25 	| Create page to see all tasks with MDDataTable      	| Program the kivymd and python files for the GUI and functionality of to see all of the data using MDDataTable                                        	| 1.5h          	|                   Mar3 	| C         	|
|      26 	| Let MDDataTable directly move to Editingscreen     	| Program python that can directry move to Editingscreen if I press one of task shown.                                                                 	| 40min         	|                   Mar3 	| C         	|
|      27 	| Let able to delete tasks in data table             	| Program python file that I can directry delete my tasks that I select in checkbox.                                                                   	| 20min         	|                   Mar3 	| C         	|
|      28 	| Let able to change color in Data table.            	| Program python file that each tasks is colored with choosen color                                                                                    	| 30min         	|                   Mar3 	| C         	|
|      29 	| Create MDColorPicker                               	| Program the kivymd and python files for the GUI and functionality to select color easelly.                                                           	| 1h            	|                   Mar3 	| C         	|
|      30 	| Create MDdatepicker                                	| Program the kivymd and python files for the GUI and functionality to select date easelly.                                                            	| 30m           	|                   Mar3 	| C         	|
|      31 	| Create MDCheckbox                                  	| Program the kivymd and python files for the GUI and functionality to select category easelly.                                                        	| 1h            	|                   Mar3 	| C         	|
|      32 	| Apply those to add page                            	| let MDColorPicker, MDDatepicker, MDCheckbox use in add page.                                                                                         	| 30m           	|                   Mar3 	| C         	|
|      33 	| Write Proposed Solution                            	| Write proposed solution.                                                                                                                             	| 2h            	|                   Mar3 	| A         	|
|      34 	| Apply those to edit page                           	| let MDColorPicker, MDDatepicker, MDCheckbox use in edit page.                                                                                        	| 40m           	|                   Mar3 	| C         	|
|      35 	| Third meeting with cliant                          	| Let cliant see the prototype and get approval.                                                                                                       	| 15m           	|                   Mar3 	| A         	|
|      36 	| Write UML diagram                                  	| Draw UML diagram with my PC.                                                                                                                         	| 40m           	|                   Mar8 	| B         	|
|      37 	| Write wireframe diagram                            	| Draw wireflame with whitebord                                                                                                                        	| 20m           	|                   Mar8 	| B         	|
|      38 	| Write System diagram                               	| Draw sustem diagram with my PC.                                                                                                                      	| 40m           	|                   Mar8 	| B         	|
|      39 	| Write flow diagrams                                	| Draw flow diagrams with whitebord                                                                                                                    	| 1h            	|                   Mar8 	| B         	|
|      40 	| Put the comment of the python code                 	| Write explanation and comments of the code in python.                                                                                                	| 1.5h          	|                   Mar8 	| C         	|
|      41 	| Make the code clean                                	| Make kivy for GUI to make more clean and organised.                                                                                                  	| 30m           	|                   Mar8 	| C         	|
|      42 	| Take a video.                                      	| Take a demonstration video.                                                                                                                          	| 20m           	|                   Mar8 	| D         	|
|      43 	| Edit a video                                       	| Edit a demonstration video                                                                                                                           	| 40m           	|                   Mar8 	| D         	|
|      44 	| Remake system diagrams                             	| Draw system diagram with the color                                                                                                                   	| 1h            	|                  Mar10 	| B         	|

## Criteria C: Coding##

### The user can register, login and logout of the system.
From here, I will show the skills that I uses for making this system.



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
I let the posts to go to the individual posts page for each posts in the lists.

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
Finally, I am able to show the data from the database, However, that data that we can see is just a text. i want to see the text, with using the Tex font style. I use MathJax to show all of those things. I set this MathJax to all pages to be able to set the all code.
```.py
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
    ......
</head>
<body onload="MathJax.typeset()">
...
```

10: H: Javascript
To post the new things, people will write the original tex code. However, user has no idea that written tex is write or wrong. So, I tried to make the program to automatically shows the things people write with passing througth tex code. I tried to do that in python code, but it is too much hard work for me. Therefore, I used Javascript to do so.
```.py
<form method="POST">
    <p>title<input id="title" type="text" name="title" onload="title_renderMath()" onchange="title_renderMath()" placeholder="enter a title" value="{{ data[2] }}"></p>
    <p>content<textarea id="test" name='content' onload="renderMath()" onchange="renderMath()" rows=”3″ cols=”50″ placeholder="enter the content">{{ data[3] }}</textarea></p>
    <input type="submit" value="Save">
</form>

......

<script>
    window.onload = function() {
        setTimeout(title_renderMath, 5);
        setTimeout(renderMath, 5);
    }
    function title_renderMath() {
        var input = document.getElementById("title").value;
        var output = document.getElementById("title_output");
        output.innerHTML = input.replace(/\n/g, "<br>");
        MathJax.Hub.Queue(["Typeset", MathJax.Hub, output]);
    }

    function renderMath() {
        var input = document.getElementById("test").value;
        var output = document.getElementById("output");
        output.innerHTML = input.replace(/\n/g, "<br>");
        MathJax.Hub.Queue(["Typeset", MathJax.Hub, output]);
    }
</script>
```

**Criterion D**


**Criterion E**
