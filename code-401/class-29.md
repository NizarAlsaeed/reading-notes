# Django Best Practices: Custom User Model

Django ships with a built-in User model for authentication. However, for a real-world project, the official Django documentation
highly recommends using a custom user model instead.

### step 1: create the project
after that, do not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.


### step 2: update settings
`AUTH_USER_MODEL = 'accounts.CustomUser' # new`

### step 3: create a model
```python
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```

### step 4: create froms:
```python
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

### step 5 : update admin.py
Finally we update admin.py since the Admin is highly coupled to the default User model.
```python
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
# DjangoX
DjangoX, which is an open-source Django starter framework
that includes a custom user model, email/password by default instead of username/email/password, social authentication, and more.

