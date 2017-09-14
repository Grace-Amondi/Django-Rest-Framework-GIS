# Django-Rest-Framework-GIS

This is a geographic add-on for django-rest-framework. By the end of this you will have a complete gis django-rest-framework. Just follow along with the steps.

**1.Create a django project**

To create a project run the following command in your terminal
```django-admin startproject geoapi```

We have named our project as geoapi. Now change directory into the project by running the following:
```cd geoapi```

**2.Create a django app**
Now we are going to create an app inside the geoapi project. This contains modls.py files as well as many other .py files.
Run this:
```django-admin startapp api```

followed by ```ls```

This will display a list of the files present in geoapi project. 
Head over to geoapi/settings.py and add api to the list of installed apps.
Run ```python manage.py runserver``` to check our progress then open 127.0.0.1:8000 in your browser and you will see a congratulations message.

**3.Create a virtual environment**

Now we will create a virtual environment:
```mkvirtualenv api```
followed by ```workon api``` (if env not activated)

**4.Install requirements**

You can do a ```pip freeze``` to check installed requirements. There is none in the meantime. There are requiremnts we need so lets install **django-rest-framework** by

```pip install djangorestframework```

then django-rest-framework-gis by 

```pip install djangorestframework-gis```

Next we need to add these to the installed apps in geoapi/settings.py file.

``` INSTALLED_APPS=[
      'rest_framework',
      'rest_framework_gis',
      ......
      ]
```

Now lets run ```python manage.py migrate```

**5.Making our project spatial**

So far so good. But it is not yet spatial. To make it geospatial head over to settings.py and add ```django.contrib.gis``` to the list of installed apps. 
We are also going to need to install pyscopg2

```pip install psycopg2```

and leaflet

```pip install django-leaflet```

add leaflet to the list of installed apps in geoapi/setting.py

Run the following command to add your installed requirements to a requirements.txt file

```pip freeze > requirements.txt```

**6.Change database to POSTGIS**

We will need to change our database to postgis
So in your terminal run first 


     
      
