```.html

<!DOCTYPE html>
<html lang="en">
<head>

<style type="text/css">
th,td {border: solid 1px;padding:5px}
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
<link rel="stylesheet" href="../static/my_style.css">
    <meta charset="UTF-8">
    {% if user %}
        <title>Profile page for {{ user[1] }}</title>
    {% else %}
        <title>User not found</title>
    {% endif %}
</head>

<body onload="MathJax.typeset()">
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


<div id="container">
<div id="left"></div>
<div id="center">

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
    <p>{{ title }}</p>
    {% if content %}
        {% for i in content %}
            <p>{{ i }}</p>
        {% endfor %}
    {% endif %}
    <p id="output"></p>

{% elif me != 0 %}
    <h2>Send message to {{ user[1] }}</h2>
    <form method="POST">
        <p>message</p>
        <p><textarea id="test" name='message' onchange="renderMath()" rows=”3″ cols=”50″ placeholder="enter the message to {{ user[1] }}" value=""></textarea></p>
        <input type="submit" value="Save">
    </form>
    <table style="border-collapse:collapse">
    <tr>
        <th>sender</th>
        <th>receiver</th>
        <th>message</th>
    </tr>
    {# template launguage jinja2 #}
    {% for c in chat %}
    <tr>
        <td>{{ c[5] }}</td>
        <td>{{ c[4] }}</td>
        <td>{{ c[3] }}</td>
    </tr>
    {% endfor %}
</table>

{% endif %}

<h2>{{ user[1] }}'s posts</h2>
{% if posts|length > 0 %}
<table style="border-collapse:collapse">
    <tr>
        <th>title</th>
        <th>content</th>
    </tr>
    {# template launguage jinja2 #}
    {% for p in posts %}
    <tr>
        <td><a href="{{ url_for('post', post_id=p[0]) }}">{{ p[2][:60] }}</a></td>
        {% if p[3] |length >= 100 %}
        <td><a href="{{ url_for('post', post_id=p[0]) }}">{{ p[3][:100] }}...</a></td>
        {% else %}
        <td><a href="{{ url_for('post', post_id=p[0]) }}">{{ p[3] }}</a></td>
        {% endif %}
    </tr>
    {% endfor %}
</table>

<h1></h1>
{% else %}
    <p>You don't have post yet.</p>
{% endif %}

<script>
    function renderMath() {
        var input = document.getElementById("test").value;
        var output = document.getElementById("output");
        output.innerHTML = input.replace(/\n/g, "<br>");
        MathJax.Hub.Queue(["Typeset", MathJax.Hub, output]);
    }
</script>

</div>
<div id="right">
    <h2>Chats</h2>
<table style="border-collapse:collapse">
    <tr>
        <th>sender</th>
        <th>receiver</th>
        <th>message</th>
    </tr>
    {# template launguage jinja2 #}
    {% for c in chats %}
    <tr>
        <td><a href="{{ url_for('get_user', userid=c[2]) }}">{{ c[5] }}</a></td>
        <td><a href="{{ url_for('get_user', userid=c[1]) }}">{{ c[4] }}</a></td>
        <td>{{ c[3][:30] }}</td>
    </tr>
    {% endfor %}
</table>
</div>
</div>
</body>
</html>


```
