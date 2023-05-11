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
Objective measurement: Verify that the registration process allows users to create an account successfully, login process grants access to the system, and logout process ends the session without any errors.
2. [issue tackled: For getting the requirements, login, register, post at the same time. Doing all of the requirements at the same page is unnecessary and difficult to use. Therefore, we needs to make multiple pages, and system to move those pages.]The user can switch between different pages.
Objective measurement: Test the functionality of page navigation by ensuring that users can easily and seamlessly move between different pages within the system without encountering errors or usability issues.
3. [issue tackled: To solve the core parts of his wants, manage his post]The system can add and edit posts, including information on title, content, and account.
Objective measurement: Test the system's ability to add new posts, verify that the required information (title, content, and associated account) is successfully stored and displayed, and ensure that editing existing posts updates the relevant information accurately.
4. [issue tackled: his wants. Tex style]The system is able to show all text with Tex font style.
Objective measurement: Evaluate whether the system consistently renders text in the desired Tex font style throughout the application, ensuring that the displayed text maintains the intended formatting and appearance.
5. [issue tackled: the wants of his creation with No3]The user can view all posts that are made by all users.
Objective measurement: Confirm that the system provides a comprehensive display of all posts created by all users, ensuring that no posts are omitted or hidden from view, and that the displayed posts are presented accurately and completely.
6. [issue tackled: For interacting and communicating with each people, chat system is the most appropriate.]The user can do the private chat between other accounts.
Objective measurement: Test the private chat functionality by verifying that users can initiate and engage in private conversations with other accounts, ensuring that messages are sent and received accurately, and that the privacy and security of the chat system are maintained.

[figure 2]The confirmation from cliant
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
<img width="968" alt="Screen Shot 2023-05-08 at 16 53 57" src="https://github.com/yutaro741/unit4/assets/111973553/6e5c0b2c-b35a-4bfc-9754-18554ead13b7">
[figure 3]System diagram of the program


**UML Diagram**
<img width="679" alt="Screen Shot 2023-05-11 at 16 45 54" src="https://github.com/yutaro741/unit4/assets/111973553/2ada6cbc-cd3c-4f6f-bc78-8510ae7d7081">
[figure 4]UML diagram of the program

**ER diagram**
![22B3ED9F-0F07-4F87-AB4A-9BF18923C2B2](https://github.com/yutaro741/unit4/assets/111973553/9681d511-fff8-4523-9ac9-9184ca2e0275)
[figure 5]ER diagram of the program

Examples of ER diagram:
users
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.32.png)
[figure 6]Example of database users
posts
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.43.png)
[figure 7]Example of databse posts
chats
![](https://github.com/yutaro741/unit4/blob/main/pictures/Screen%20Shot%202023-05-09%20at%2017.30.49.png)
[figure 8]Example of databse chats

**Flow Diagrams**
![A9914D51-A74E-4DA3-A5E6-01B8F898EBC3](https://github.com/yutaro741/unit4/assets/111973553/8b172ce7-7d22-4fc0-9b99-a16c840e3e98)
[figure 9]Flow diagram of login system
![DEB3AF55-00A0-49B7-BA8C-DDEBC76E5B6F](https://github.com/yutaro741/unit4/assets/111973553/8e62166b-674f-4fcc-88b7-279d7295440a)
[figure 10]Flow diagram of register system
![137432FA-7F43-4640-9E50-ABF4B967BFF7](https://github.com/yutaro741/unit4/assets/111973553/884824f5-6de0-4b70-b94c-f7874ae7e2ba)
[figure 11]Flow diagram of post page(update)
![828017DE-25FA-4E4A-97E5-21FE412AE142](https://github.com/yutaro741/unit4/assets/111973553/b5b86a8c-3cf1-4add-a637-5cc67215bddf)
[figure 12]Flow diagram of post page(open)
![66435369-489A-470A-8156-88EC4EEDFF73](https://github.com/yutaro741/unit4/assets/111973553/e973e96e-31e5-4eb2-adcc-54dbbf98f45c)
[figure 13]Flow diagram of profile page


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

[figure 14] Record of tasks

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

[figure 15]test plan
## Criteria C: Coding
Things I used for this website:
Python
-Flask
-database_handler(from unit3)
HTML&CSS
-MathJax
SQLite

List of techneque:
### setup
```.py
from flask import Flask, render_template, request, redirect, url_for, make_response
from my_lib import database_handler
app = Flask(__name__)
@app.route("/login")
def login():
    return render_template("login.html")
if __name__ == '__main__':
    app.run()#run the program here.
```
I set up python file with importing Flask. Also, I used database_handler, that I used last project(project3). Please see that part for the additional things.
The program above is the code to run the program and make the development website. It will show the login.html, and the name of the link is /login.
So, next step is to make HTML file.

```.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="../static/my_style.css">
</head>
<body>
<p>This is login screen</p>
</body>
</head>
```
This login.html file is the very first setting of the login system. This shows the message "This is the login screen" in the website.
Also, this will import my_style.css from the coding, to improve how it shows in the website.

I wrote so many CSS code in the project, but it is just the change in GUI, so I will not shows in this criteria C. If you want to see the dtails, please see the codes.

Also, I made the database(users, posts, chats) for the part. The prosess of making database is in the previous project, so please see that.

<img width="235" alt="Screen Shot 2023-05-10 at 16 35 50" src="https://github.com/yutaro741/unit4/assets/111973553/f9643d08-8d27-4230-b070-bacbe7947925">

[figure 16]The daatabases

### SC1: The user can register, login and logout of the system.
From here, I will show the skills that I uses for making this system.
For making those registeration screen, I used flasks methods(get, post), request and cookies. 
Methods: For using it, I can know that user pressed the button(or any other dynamic processing) or not.
Cookies: It used to store small amounts of data in the user's browser, which can be used to maintain the user's state across multiple requests. This time I used as saving user id.
request: You ca get the text from HTML and able to use inside the program.
Also, I used the database_handler from previous project(unit3 project), so go to unit3 if you need an detail.

For example, I have code like this for login system:
app.py:
```.py
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
    return render_template("login.html")
```

Also, I write the html for putting in the data. Below is the login.html
```.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Welcome to the best SNS</title>
    <link rel="stylesheet" href="../static/my_style.css">
</head>
<body onload="MathJax.typeset()">
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
</body>
</html>
```
I used the techenique of class, that can change how it shows in from CSS. Also, I write a method=post to send a data that form is completed into python.
So, with writting the html and css, I could be able to show in the website. I could see those kind of screen.

<img width="445" alt="Screen Shot 2023-05-10 at 16 31 28" src="https://github.com/yutaro741/unit4/assets/111973553/1e987b3a-131d-4ce7-93db-6fa91ffc0c42">

[figure 17]login screen

For registration page, I just added password check for the account. For the logout system, I even didn't make a page. I just expire the cookie. Please watch the movie for details.


### SC2: The user can switch between different pages.
As was a bit in the previous code, the page can be moved by render_template(). Also, To work with a coding, redirect(url_for()) is also useful.
However, I need a button for changing the screen. So, I made the header that I can used for all of the pages, and change the pages.

(all)HTML file:
```.html
<header class="site-header">
  <div class="wrapper site-header__wrapper">
    <a href="{{ url_for('main') }}" class="brand">`PostMath`</a>
    <nav class="nav">
      <ul class="nav__wrapper">
        <li class="nav__item"><a href="{{ url_for('main') }}">Home</a></li>
          {% if user_id!=0 %}
          <li class="nav__item"><a href="{{ url_for('logout') }}">Logout</a></li>
          <li class="nav__item"><a href="{{ url_for('get_user', userid=user_id)}}">Account</a></li>
          {% else %}
          <li class="nav__item"><a href="{{ url_for('login') }}">Login</a></li>
          <li class="nav__item"><a href="{{ url_for('registration') }}">Register</a></li>
          {% endif %}
      </ul>
    </nav>
  </div>
</header>
```
The part that I was struggled is the heading. I need to show "login" and "register" button when user is not logined. However, I need to show "logout" button when user is logined alleady. So, I used template launguage called jinja2 to do simple if statement inside the python. Also, I add the button called "account" that can go to the profile page of logined account, for not only stopping the changes for losing one button with logining, but also getting easier to move inside the website.

However, I need the user_id, that needs to be sended from python file, so I make it from here. I will just add the code that get the user id from cookie and send it to the html.
```.py
@app.route("/everything")
def ~~~~~():
    ~~~~~~~~~~~~~
    if request.cookies.get('user_id'):
        user_id = request.cookies.get("user_id")
    return render_template("login.html", user_id=user_id)
```

This is the result.
If the user is not logined:

<img width="1680" alt="Screen Shot 2023-05-10 at 16 45 21" src="https://github.com/yutaro741/unit4/assets/111973553/70cccef4-dc3a-4be2-a273-5f8a20d55fc2">

[figure 18]Header when user is not logined

If the user is logined:

<img width="1680" alt="Screen Shot 2023-05-10 at 16 45 29" src="https://github.com/yutaro741/unit4/assets/111973553/bd71731c-0105-4841-895d-9ac52ec6bf0f">

[figure 19]Header when user logined

So, the website gets very easy to change the screen from one and onother.

### SC4: The user can view all posts that are made by all users.
Because I make from main page, I will explain success criteria No4 faster than No3.
For showing all of the pages, I need to get all of the data from database, by using sqlite. That is easy-I did so many times in this/last project-, but showing all of that data is not easy. So, I use jinja2 to use "for loop" inside the HTML to make a table and show everything from the database.
Also, I used the SQLite with for loop to make the list that has username(database posts has only user_id).
Additionally, if the title is too long, I cut it out and place "...".
python:
```.py
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
    ~~~
```

HTML:
```.html
~~~~
<div id="center">
<h1>table of posts</h1>
<table style="border-collapse:collapse">
    <tr>
        <th>author</th>
        <th>title</th>
    </tr>
    {% for i in posts %}#Use for loop!!!
        <tr>
            <th><a href="{{ url_for('get_user', userid=i[1]) }}">{{ i[4] }}</a></th>
            <th><a href="{{ url_for('post', post_id=i[0]) }}">{{ i[2] }}</a></th>
        </tr>
    {% endfor %}
</table>
</div>
~~~~
```
So, I could make the main page to be able to go to the post.(look like this)

<img width="1250" alt="Screen Shot 2023-05-10 at 17 35 02" src="https://github.com/yutaro741/unit4/assets/111973553/81cf36ff-d3f5-419a-8c49-72dde87a8899">

[figure 20]The main screen

Also, I made the each table to be able to link to the post page(that will show afterwords) and profile page.

In the profile page, I will make the page that shows all of the post that made by the specific user. By doing that, It will be getting easy to show and search about the posts.
The way to make the profile page is mostly same, and just limit the things that shows from the posts, so I will not show you a code. 
The results gets like this.

<img width="830" alt="Screen Shot 2023-05-10 at 17 36 03" src="https://github.com/yutaro741/unit4/assets/111973553/65cd101c-aece-463c-a792-d5193945f788">

[figure 21]profile page


### SC3. The system can add and edit posts, including information on title, content, and account.
For the next step, to add the post, I decided to be able to post in the page that can see the profile.
That means, If user go to the profile page, that is same page as logined user, you can see the special screen for posting.
So, this is the program for html.
```.html
{% if me == user[0] %}
    <h1>Welcome, {{ user[1] }}</h1>
    <h2>create a new post</h2>
    <form method="POST">
        <p>title</p>
        <p><input type="text" name="title" placeholder="enter a title" value="" rows=”1″ cols=”300″></p>
        <p>content</p>
        <p><textarea id="test" name='content' onchange="renderMath()" rows=”20″ cols=”300″ placeholder="enter the content" value=""></textarea></p>
        <input type="submit" value="Save">
    </form>
    {% endif %}
    <p id="output"></p>
```
```.py
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
    ~~~~~~
```
So, I am able to make the program that shows entering screen. the results is like this. I am logining with account called "z"

<img width="793" alt="Screen Shot 2023-05-10 at 17 02 07" src="https://github.com/yutaro741/unit4/assets/111973553/6bede219-3b13-42f2-8ce6-b778f1d4d07c">

[figure 22]improved profile page(same account)

Shows the screen that can post something.

<img width="806" alt="Screen Shot 2023-05-10 at 17 02 29" src="https://github.com/yutaro741/unit4/assets/111973553/5b95ca7f-14d5-4c62-8acb-fac6ffd1a1d5">

[figure 21]improved profile page(different account)

Do not shows the post screen. Instead of that, I will show the private chat between them.(write afterwords)

Now, we can see the list of the posts and able to upload it. However, there is no meaning if you can't see all of the posts, or edit a posts. So, I will make onother place that can see the post, and also to be able to edit that post if the post is logined post.
For doing that, I used the tequenique for find out the post id with "link". I let the link to do like /post/19, if the post id is 19. Therefore, user, and developer can both know what is the post id.
```.py
app.route("/post/<post_id>",  methods=['GET', 'POST'])
def post(post_id):
    db = database_handler()
    data = db.get_info(f"""SELECT * from posts WHERE id={post_id}""")
    if not request.cookies.get("post_id"):#Save the post id into cookie.
        resp = make_response(redirect(url_for("post", post_id=post_id)))
        resp.set_cookie('post_id', f"{post_id}")
        return resp
        
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
```
There is no special tequnique that I used for the html, so I will just cut it out today.

Results
if you have different account/not logined:

<img width="834" alt="Screen Shot 2023-05-10 at 17 44 43" src="https://github.com/yutaro741/unit4/assets/111973553/9daa2e34-060c-4a55-b454-6b2cd2b38976">

[figure 23]post page(not logined)

if you are logined with the account that posted:

<img width="819" alt="Screen Shot 2023-05-10 at 17 45 09" src="https://github.com/yutaro741/unit4/assets/111973553/50f19415-af88-45f9-af3e-c4aee0277de1">

[figure 24]post page(logined)

So, in this criteria, I am able to add/edit/see the posts.

### SC5: The system is able to show all text with Tex font style.
The formulas were casually in the picture, but this is the thing that must be done with a hard work.
For this time, I used the things called MathJax, to be able to use in the HTML file.
All HTML file:
```.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
</head>
<body onload="MathJax.typeset()">

##INSIDE code will all get scanned by MathJax(=latex).

</body>
</html>
```
Thats why, I am able to show the beautiful math formulas in the post page. 
However, the problem remains. MathJax shows only the things in text. It will not convert the things that is writting inside the form(specially textbox).
So, I need to make a program that automatically shows the things that I write. But it is quite hard. Python can do the program that run only when the page reload.
The searvice that will automatically reloaded each time user typed a letter is horrifying. So, I chosed to use Javascript for the single part.
post/profile.html
```.html
~~~
<form method="POST">
    <p>title<input id="title" type="text" name="title" onload="title_renderMath()" onchange="title_renderMath()" placeholder="enter a title" value="{{ data[2] }}"></p>
    <p>content<textarea id="test" name='content' onload="renderMath()" onchange="renderMath()" rows=”3″ cols=”50″ placeholder="enter the content">{{ data[3] }}</textarea></p>
    <input type="submit" value="Save">
</form>
<h2 id="title_output"></h2>
<p id="output"></p>
~~~

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
~~~
```
This program shows if there is any update in the form, and if there is reload in the form, the text will appear and shows the same things that is written in the textbox below the form, with the Latex.
Because of this, user can see the posts that passes the Latex. Therefore, the user can check the Latex is working properlly, and able to check that there is no typing mistake.

Results:

<img width="819" alt="Screen Shot 2023-05-10 at 17 45 09" src="https://github.com/yutaro741/unit4/assets/111973553/28b59b7b-3e13-49a1-aa67-d0005298678d">

[figure 25]post edit page when opened

<img width="788" alt="Screen Shot 2023-05-10 at 18 07 09" src="https://github.com/yutaro741/unit4/assets/111973553/c427a762-5505-42ad-8d49-692011cfbde0">

[figure 26]post edit page when edited

It automatically shows the posts with latex! amazing!

### The user can do the private chat between other accounts.
This one is not that hard. I just make an option in profile page, -if the user is logined but not the same accout with the profile page- that can send the messsage to user in profile page.
I can just place the message on the right side on the page. Specificlly, in the profile page, I can show the message that made with logined user and user that is in profile page.
I use the for loop to find the username of each user, and for loop with html for showing that data.

For example, profile page python code:
```.py
~~~
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
~~~
```
profile.html:
```.html
~~~
{% for c in chat %}
    <tr>
        <td>{{ c[5] }}</td>
        <td>{{ c[4] }}</td>
        <td>{{ c[3] }}</td>
    </tr>
{% endfor %}
~~~
```
As the results, I can see the all of the chats at the side of the website.

<img width="1680" alt="Screen Shot 2023-05-10 at 18 13 10" src="https://github.com/yutaro741/unit4/assets/111973553/c79dd95b-ad67-4b99-9b7f-ff3487437a8e">

[figure 27]final profile page

## Criterion D
Video
https://drive.google.com/drive/folders/1B4tLp6y72Nwf5ufOqXBKxAgS3HBtt_As?usp=sharing
Script
https://docs.google.com/document/d/17RhwhugTgnyRK-7lTkffVPCr8CJ9haByb5E0chXQdec/edit?usp=sharing

## Criterion E

memo:https://docs.google.com/document/d/1sO78bfn9AhxLug2k9wMZJWI4IzSHBWK3ixWrDTtXOng/edit?usp=sharing

Feedback from cliant:
| Cliant 	| Success criteria                                                                         	| Sccessed or not(out of 3) 	| Feedback                                                        	| Further development                                                                                                	|
|--------	|------------------------------------------------------------------------------------------	|---------------------------	|-----------------------------------------------------------------	|--------------------------------------------------------------------------------------------------------------------	|
|      1 	| The user can register, login and logout of the system.                                   	|                         3 	| Perfect                                                         	| N/A                                                                                                                	|
|      2 	| The user can switch between different pages.                                             	|                         3 	| Perfect                                                         	| Make searching system. Also development of GUI                                                                     	|
|      3 	| The system can add and edit posts, including information on title, content, and account. 	|                         2 	| I didn't say it, but able to delete as well.                    	| Able to delete posts easelly.                                                                                      	|
|      4 	| The system is able to show all text with Tex font style.                                 	|                       100 	| It was better than I thought.                                   	| Make rotation thingy.                                                                                              	|
|      5 	| The user can view all posts that are made by all users.                                  	|                         3 	| Good, but I also want to have a searching system                	| Searching system.                                                                                                  	|
|      6 	| The user can do the private chat between other accounts.                                 	|                         3 	| It is problem that you can't send the message that is too long. 	| Make it able to send long message. Let it possible to block someone/change setting to not be able to send message. 	|

[figure 28]The list of feedback from cliants

| Person G 	| Success criteria                                                                         	| Sccessed or not(out of 3) 	| Feedback                      	| Further development                             	|
|----------	|------------------------------------------------------------------------------------------	|---------------------------	|-------------------------------	|-------------------------------------------------	|
|        1 	| The user can register, login and logout of the system.                                   	|                         3 	| Perfect                       	| N/A                                             	|
|        2 	| The user can switch between different pages.                                             	|                         3 	| Perfect                       	| Maybe the bookmark system                       	|
|        3 	| The system can add and edit posts, including information on title, content, and account. 	|                         2 	| why no delete?                	| Delete system, and be not                       	|
|        4 	| The system is able to show all text with Tex font style.                                 	| ?                         	| Don't know about tex writing. 	| N/A                                             	|
|        5 	| The user can view all posts that are made by all users.                                  	|                         2 	| Why no searching?             	| Searching system                                	|
|        6 	| The user can do the private chat between other accounts.                                 	|                         3 	| want to send to multiple user 	| Let able to make a group between multiple user. 	|

[figure 29]The list of feedback from person G

**Recommendation 1**
Even on the small scale I made had so far, we sometimes lose track of which post I wrote on, and it should get harder and harder as the number of users grows. Also, with the previous way of updating by post-id, the new ones keep moving up and the old ones are not seen. So, as mentioned in the feedback, I will recommend to create a feature that allows users to search for post.

Specifically, the things that allows sorting and a things that allows searching by word. For the sorting thing, I will make it possible to search by ranking of the number of views at different times of the day, weeks and the month. in addition to the previous sorting where the newest posts are always at the top.
Also, for the word-by-word search, simply type in a word to search for sites that contain that word. Also, perhaps a tag function (#linear algebra, #geometry, ...) could be created to make it easier to search.

**Recommendation 2**
Second, the chat function could be improved. Currently, with the small number of people using it, it is not a problem, but in the next phase, people who post well-known posts may be mass-messaged by several people. There is also the possibility of spam or other malicious people sending large numbers of messages.
Therefore, I would like to do a customization of the chat system and increase security. Specifically, the code to add a settings feature to the profile feel screen to turn off the chat, and prevent certain people from sending chats.

As a further development, I would also like to create a function to judge bad language, spam, etc. Specifically, a program that judges bad language and disables chatting with that person, or/and a program that sends a warning message or disables chatting with people who send multiple or large numbers of messages at once.
