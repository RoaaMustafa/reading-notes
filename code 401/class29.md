#  Django Custom User

## AbstractUser vs AbstractBaseUser

AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. 

 AbstractUser which actually subclasses AbstractBaseUser but provides more default configuration.
 
 ### Custom User Model
 + update config/settings.py
 + create a new CustomUser model
 + create new UserCreation and UserChangeForm
 + update the admin

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
..........................................
AUTH_USER_MODEL = 'accounts.CustomUser' # new
```
Now update models.py with a new User model which we'll call CustomUser.
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

 create a new file in the accounts app called forms.py
 
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
 Finally we update admin.py since the Admin is highly coupled to the default User model.
 
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
 
 And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.
 
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
 
 ```
 
 # config/settings.py
LOGIN_REDIRECT_URL = 'home'
LOGOUT_REDIRECT_URL = 'home'
 ```
 
 Create a new project-level templates folder and within it a registration folder as that's where Django will look for the log in template. We will also put our signup.html template in there.
 
 
 
