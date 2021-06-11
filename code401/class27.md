# Read : 27

## Django Models

- Django web applications access and manage data through Python objects referred to as models.

- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.


### Model Primer

**Model definition**

- Models are usually defined in an application's `models.py` file.

- They are implemented as subclasses of `django.db.models.Model`, and can include fields, methods and metadata.

- The code fragment below shows a "typical" model, named `MyModelName`:

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

**Fields**

- `my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`

- A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables.

- Each database record (row) will consist of one of each field value.

- `max_length=20` — States that the maximum length of a value in this field is 20 characters.
- `help_text='Enter field documentation'` — provides a text label to display to help users know what value to provide when this value is to be entered by a user via an HTML form.

**Metadata**

```
class Meta:
    ordering = ['-my_field_name']
```

- You can declare model-level metadata for your Model by declaring `class Meta`, as shown.

- One of the most useful features of this metadata is to control the default ordering of records returned when you query the model type.


**Methods**

```
def __str__(self):
    return self.field_name
```

- Minimally, in every model you should define the standard Python class method __str__() to return a human-readable string for each object.

```
def get_absolute_url(self):
    """Returns the url to access a particular instance of the model."""
    return reverse('model-detail-view', args=[str(self.id)])
```

- Another common method to include in Django models is `get_absolute_url()`, which returns a URL for displaying individual model records on the website *(if you define this method then Django will automatically add a "View on Site" button to the model's record editing screens in the Admin site)*.
  


  
##### [Go Back](code_401_reading_notes.md)