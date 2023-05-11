```.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Math Posts!</title>
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
<div id="left">
<h1>table of users</h1>
<table style="border-collapse:collapse; border: 1px solid black">
    <tr>
        <th class="num">id</th>
        <th>username</th>
    </tr>
    {# template launguage jinja2 #}
    {% for u in all_users %}
    <tr>
        <td><a href="{{ url_for('get_user', userid=u[0]) }}">{{ u[0] }}</a></td>
        <td><a href="{{ url_for('get_user', userid=u[0]) }}">{{ u[1] }}</a></td>
    </tr>
    {% endfor %}
</table>
</div>

<div id="center">
<h1>table of posts</h1>
<table style="border-collapse:collapse">
    <tr>
        <th>author</th>
        <th>title</th>
    </tr>
    {% for i in posts %}
        <tr>
            <th><a href="{{ url_for('get_user', userid=i[1]) }}">{{ i[4] }}</a></th>
            <th><a href="{{ url_for('post', post_id=i[0]) }}">{{ i[2] }}</a></th>
        </tr>
    {% endfor %}
</table>
</div>


<div id="right">
{% if user_id != 0 %}
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
{% endif %}
</div>

</div>

</body>
</html>


```
