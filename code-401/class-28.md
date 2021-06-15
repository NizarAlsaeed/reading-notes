# Django Tutorial Part 9: Working with forms

Django Forms take a lot of the work oufrom django import forms

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")
t of all these steps, by providing a framework 
that lets you 


define forms and their fields programmatically, and then use these objects to
both generate the form HTML code and handle much of the validation and user interaction.

### Form

The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values,
valid values, and (once validated) the error messages associated with invalid fields.

 The class also provides methods for rendering itself in templates using predefined formats (tables, lists, etc.) or for 
 getting the value of any element (enabling fine-grained manual rendering).
 
 
 Form data is stored in an application's forms.py file, inside the application directory
 
 ```python
 from django import forms

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

 ```
 
 ### validation
 
 inside a method, you can wrtie your logic to validate the form input and when there is something invald just raise this exception 
 `raise ValidationError(_('Invalid date - renewal in past'))` 
 
 
 remember tht you need to import the following:
 
 ```python
from django.core.exceptions import ValidationError
from django.utils.translation import ugettext_lazy as _

# ValidationError, specifying the error text that we want to display in the form if an invalid value is entered. 
#The example above also wraps this text in one of Django's translation functions ugettext_lazy() 
#(imported as _()), which is good practice if you want to translate your site later.

```

### view

For forms that use a POST request to submit information to the server, the most common pattern is for the
view to test against the POST request type `(if request.method == 'POST':)` 
to identify form validation requests and GET (using an `else` condition) to identify the initial form creation request.
