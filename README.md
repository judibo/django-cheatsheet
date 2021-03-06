# django-cheatsheet

## How to create a new Django project
```bash
django-admin startproject projectname
```

## How to start the Django development server
```bash
python3 manage.py runserver
```

## How to create a new application in the project
```bash
python3 manage.py startapp
```
## But how do I stop it?
```bash
CTRL + C
```

## Django Directiory Structure
```
djangoproject
|
|- djangoproject
|  |
|  |- settings.py: Main settings for project (db, apps, config, etc.)
|  |- urls.py: Main URLs for entire project
|
|- application_name
|  |- static: (dir) Holds all static files (css, js, images, auxiliar forms)
|  |- templates: (dir) Holds all HTML template files
|  |- migrations: This holds all data migration files
|  |- admin.py: This is where we register data models
|  |- models.py: This is where we put all data models
|  |- views.py: This is where we put the functions that run our routes
|  |- urls.py: Every URL for our site is defined here
|
|- manage.py: Let's us manage everything about our project
```

## How to make URLs with the path() function:
```python
urlpatterns = [
  path('route/', views.route_name, name='route_name'), 
  path('route2/<string_variable>', views.route2_name, name='route2_name'),
  path('route3/<int:variable_name>', views.route3_name, name='route3_name'),
]
```

## How to make a view funtion:
```python
def route1_name(request):
    return render(request, 'template.html')

def route2_name(request, string_variable):
    return render(request, 'template2.html', {'data': string_variable}) 
    
def route3_name(request, variable_name):
    return render(request, 'template3.html', {'data': variable_name}) 
```
