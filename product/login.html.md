This is login.html

```.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Welcome to the best SNS</title>
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
