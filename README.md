django-authen 2.0.0
--------------------

Authen is a simple Django **login** and **logout** page written with **bootstrap-4**

Quick start
-----------

1. How to install
```
     pip install django-authen
```

2. Add **authen** **django_python3_ldap** and to your INSTALLED_APPS in **settings.py**
```
    INSTALLED_APPS = [
        ...
        'django_python3_ldap',
        'authen',
    ]
```

3. Include the **authen** urls in your projects **urls.py**
```
    path('authen/', include('authen.urls')),
```

4. Set **LOGIN_URL** to authen login url in **settings.py**
```
    LOGIN_URL = "/authen/login/"
``` 
5. Set **AUTHEN** configuration in **settings.py**
```
    AUTHEN = {
        "COMPANY_NAME": "Your Company Name",
        "LOGIN_TITLE": "Login w/ your id",
        "LOGOUT_TITLE": "Logged out.",
        "LOGOUT_MESSAGE": "Thanks for spending some quality time with the our site today.",
    }
```
5. Finally run migration
```
    python manage.py migrate 
```

6. Visit `/authen/login/` for login and `/authen/logout/` for logout page on browser.

-----------

Screenshots
-----------

|           login            |
|----------------------------|
| ![login](assets/login.png) |

|           logout           |
|----------------------------|
|![logout](assets/logout.png)|

-----------
 ```   
Copyright 2018 semiworld.org

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
