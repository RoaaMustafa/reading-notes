#  [Django Custom User](https://learndjango.com/tutorials/django-custom-user-model)

The authentication that comes with Django is good enough for most common cases, but you may have needs not met by the out-of-the-box defaults. Customizing authentication in your projects requires understanding what points of the provided system are extensible or replaceable.

## AbstractUser vs AbstractBaseUser

 In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. 

 AbstractUser which actually subclasses AbstractBaseUser but provides more default configuration.
 
 ## [Setting up and development](https://github.com/RoaaMustafa/reading-notes/blob/main/code%20401/class29.md)
 
 ### Custom User Model
 
 + update config/settings.py
 + create a new CustomUser model
 + create new UserCreation and UserChangeForm
 + update the admin


### config/settings.py
```
# config/settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'accounts', # new
]
AUTH_USER_MODEL = 'accounts.CustomUser' # new
```

### Now update models.py with a new User model which we'll call CustomUser.

```
# accounts/models.py
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```

 ### create a new file in the accounts app called forms.py
  ### accounts/forms.py
  
 ```
 
 # accounts/forms.py
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm
from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')
 ```
 
 ### Finally we update admin.py since the Admin is highly coupled to the default User model.
 ###  accounts/admin.py
 
 ```
 # accounts/admin.py
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ['email', 'username',]

admin.site.register(CustomUser, CustomUserAdmin)
 ```
 
 ### And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.
 ###   config/settings.py
 
 ```
 # config/settings.py
TEMPLATES = [
    {
        ...
        'DIRS': [str(BASE_DIR.joinpath('templates'))], # new
        ...
    },
]
 ```
 
 ### config/settings.py
 
 ```
 
# config/settings.py
LOGIN_REDIRECT_URL = 'home'
LOGOUT_REDIRECT_URL = 'home'
 ```
 
 ### Create a new project-level templates folder and within it a registration folder as that's where Django will look for the log in template. We will also put our signup.html template in there.
 
 ### creating templates 
 
 ```
(accounts) $ touch templates/registration/login.html
(accounts) $ touch templates/registration/signup.html
(accounts) $ touch templates/base.html
(accounts) $ touch templates/home.html
```

### templates/base.html

```
<!-- templates/base.html -->
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>{% block title %}Django Auth Tutorial{% endblock %}</title>
</head>
<body>
  <main>
    {% block content %}
    {% endblock %}
  </main>
</body>
</html>
```

###  templates/home.html


```
<!-- templates/home.html -->
{% extends 'base.html' %}

{% block title %}Home{% endblock %}

{% block content %}
{% if user.is_authenticated %}
  Hi {{ user.username }}!
  <p><a href="{% url 'logout' %}">Log Out</a></p>
{% else %}
  <p>You are not logged in</p>
  <a href="{% url 'login' %}">Log In</a> |
  <a href="{% url 'signup' %}">Sign Up</a>
{% endif %}
{% endblock %}

```

###  templates/registration/signup.html


```

<!-- templates/registration/signup.html -->
{% extends 'base.html' %}

{% block title %}Sign Up{% endblock %}

{% block content %}
<h2>Sign Up</h2>
<form method="post">
  {% csrf_token %}
  {{ form.as_p }}
  <button type="submit">Sign Up</button>
</form>
{% endblock %}
```

### config/urls.py


```
# config/urls.py
from django.contrib import admin
from django.urls import path, include
from django.views.generic.base import TemplateView

urlpatterns = [
    path('', TemplateView.as_view(template_name='home.html'), name='home'),
    path('admin/', admin.site.urls),
    path('accounts/', include('accounts.urls')),
    path('accounts/', include('django.contrib.auth.urls')),
]
```



### accounts/urls.py


```
# accounts/urls.py
from django.urls import path
from .views import SignUpView

urlpatterns = [
    path('signup/', SignUpView.as_view(), name='signup'),
]
```


###  accounts/views.py


```
# accounts/views.py
from django.urls import reverse_lazy
from django.views.generic.edit import CreateView

from .forms import CustomUserCreationForm

class SignUpView(CreateView):
    form_class = CustomUserCreationForm
    success_url = reverse_lazy('login')
    template_name = 'registration/signup.html'
```


## [djangox](https://github.com/wsvincent/djangox)

Another way of using django. Convention over configuration for urls, mako template language support,json response, REST... Visit Snyk Advisor to see a full health score report for djangox, including popularity, security, maintenance & community analysis.


There is a temptation for me to continue adding features to DjangoX such as integration with PostgreSQL/Docker, environment variables, third-party packages like django-debug-toolbar and django-extensions, admin hardening, and more. 




### Instullation 

```
$ git clone https://github.com/wsvincent/djangox.git
$ cd djangox
```

### Pip
```
$ python3 -m venv djangox
$ source djangox/bin/activate
(djangox) $ pip install -r requirements.txt
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver
# Load the site at http://127.0.0.1:8000
```

### Pipenv

```
$ pipenv install
$ pipenv shell
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver
# Load the site at http://127.0.0.1:8000
```

### Docker


```
$ docker build .
$ docker-compose up -d
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
# Load the site at http://127.0.0.1:8000

```
