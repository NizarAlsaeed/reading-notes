# Django Tutorial Part 3: Using models
Before you jump in and start coding the models, it's worth taking a few minutes
to think about what data we need to store and the relationships between the different objects.

Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, 
and can include fields, methods and metadata.

## Features inside the model:

### Fields

A model can have an arbitrary number of fields, of any type — each one represents a column of data .

`my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`

### Metadata

You can declare model-level metadata for your Model by declaring class Meta, as shown. 

```
class Meta:
    ordering = ['-my_field_name']
```

One of the most useful features of this metadata is to control the default ordering of records returned when you query the model type.

### Methods

A model can also have methods.

# Django Tutorial Part 4: Django admin site

The admin application can also be useful for managing data in production, depending on the type of website.


### Registering models
Register the models by copying the following text into the bottom of the file. This code imports the models and then 
calls admin.site.register to register each of them.

You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.

`python3 manage.py createsuperuser`

