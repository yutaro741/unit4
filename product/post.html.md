```.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>POST of {{ data[2] }}</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>
    <link rel="stylesheet" href="../static/my_style.css">
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

{% if is_user %}
<h2>Edit a post</h2>
<form method="POST">
    <p>title<input id="title" type="text" name="title" onload="title_renderMath()" onchange="title_renderMath()" placeholder="enter a title" value="{{ data[2] }}"></p>
    <p>content<textarea id="test" name='content' onload="renderMath()" onchange="renderMath()" rows=”3″ cols=”50″ placeholder="enter the content">{{ data[3] }}</textarea></p>
    <input type="submit" value="Save">
</form>

<p>{{ title }}</p>
{% if content %}
    {% for i in content %}
        <p>{{ i }}</p>
    {% endfor %}
{% endif %}
<h2 id="title_output"></h2>
<p id="output"></p>

{% else %}
<p>user id:{{ data[1] }}</p>
<h2>{{ data[2] }}</h2>
<p>{{ data[3] }}</p>

{% endif %}
</div></div>

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

</body>
</html>

```
