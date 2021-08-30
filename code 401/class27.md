
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
  
  
