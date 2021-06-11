# Read : 26

## Intro to Django


- **What is Django?**

  - Django is a high-level Python web framework that enables rapid development of secure and maintainable websites.

  - Built by experienced developers, Django takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. 

  - It is free and open source, has a thriving and active community, great documentation, and many options for free and paid-for support.


- **What does Django code look like?**

  - **URLs:** A URL mapper is used to redirect HTTP requests to the appropriate view based on the request URL. The URL mapper can also match particular patterns of strings or digits that appear in a URL and pass these to a view function as data.

  - **View:** A view is a request handler function, which receives HTTP requests and returns HTTP responses.

  - **Models:** Models are Python objects that define the structure of an application's data, and provide mechanisms to manage (add, modify, delete) and query records in the database.

  - **Templates:** A template is a text file defining the structure or layout of a file (such as an HTML page), with placeholders used to represent actual content.


### Sending the request to the right view *(urls.py)*
```
urlpatterns = [
    path('admin/', admin.site.urls),
    path('book/<int:id>/', views.book_detail, name='book_detail'),
    path('catalog/', include('catalog.urls')),
    re_path(r'^([0-9]+)/$', views.best),
]
```


### Handling the request *(views.py)*
```
from django.http import HttpResponse
def index(request):
    # Get an HttpRequest - the request parameter
    # perform operations using information from the request.
    # Return HttpResponse
    return HttpResponse('Hello from Django!')
```


### Defining data models *(models.py)*
```
from django.db import models
class Team(models.Model):
    team_name = models.CharField(max_length=40)
    TEAM_LEVELS = (
        ('U09', 'Under 09s'),
        ('U10', 'Under 10s'),
        ('U11', 'Under 11s'),
        ...  #list other team levels
    )
    team_level = models.CharField(max_length=3, choices=TEAM_LEVELS, default='U11')
```


### Querying data *(views.py)*
```
from django.shortcuts import render
from .models import Team
def index(request):
    list_teams = Team.objects.filter(team_level__exact="U09")
    context = {'youngest_teams': list_teams}
    return render(request, '/best/index.html', context)
```


### Rendering data *(HTML templates)*
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Home page</title>
</head>
<body>
  {% if youngest_teams %}
    <ul>
      {% for team in youngest_teams %}
        <li>{{ team.team_name }}</li>
      {% endfor %}
    </ul>
  {% else %}
    <p>No teams are available.</p>
  {% endif %}
</body>
</html>
```


##### [Go Back](code_401_reading_notes.md)