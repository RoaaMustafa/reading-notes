
# Django Models

 Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc. 
 
 
 ### Model definition
 
 Models are usually defined in an application's models.py file. 
 They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata. 
 The code fragment below shows a "typical" model, named MyModelName:

 ## Designing the LocalLibrary models
 
  Django allows you to define relationships that are one to one (**OneToOneField**), one to many (**ForeignKey**) and many to many (**ManyToManyField**).
  
  the UML association diagram below shows the models :
  
  ![UML association diagram ](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models/local_library_model_uml.svg)
  
  The diagram also shows the relationships between the models, including their multiplicities.
  
  ```
  from django.db import models

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta:
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the url to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name
  ```
  
  ### Fields
  `my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')  `
  
  we are giving our field two arguments:

`max_length=20` — States that the maximum length of a value in this field is 20 characters.


`help_text='Enter field documentation'` — provides a text label to display to help users

### Metadata
You can declare model-level metadata for your Model by declaring class Meta, as shown.
  ```
    class Meta:
    ordering = ['-my_field_name']
  ```
    
    **__str__()** to return a human-readable string for each object. 
    
   ## Defining the LocalLibrary Models
   
   `from django.db import models `
+ Copy the Genre model code shown below and paste it into the bottom of your models.py file.
+ The Book model represents all information about an available book in a general sense, but not a particular physical "instance" or "copy" available for loan. The model uses a CharField to represent the book's title and isbn
+ The BookInstance represents a specific copy of a book that someone might borrow, and includes information about whether the copy is available or on what date it is expected back, "imprint" or version details, and a unique id for the book in the library.    
+ The BookInstance represents a specific copy of a book that someone might borrow, and includes information about whether the copy is available or on what date it is expected back, "imprint" or version details, and a unique id for the book in the library.
+ Copy the Author model (shown below) underneath the existing code in models.py.

## Re-run the database migrations

```
python3 manage.py makemigrations
python3 manage.py migrate
```


# Django Admin

+ he Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. 
+ he admin application can also be useful for managing data in production, depending on the type of website. 

## Registering models 
`from django.contrib import admin `



    
