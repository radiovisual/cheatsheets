# Django

## Django Quickstart

Quick start assumes you have [python](https://www.python.org/downloads/) and [Django](https://docs.djangoproject.com/en/1.9/topics/install/) installed. This quickstart is a condensed version of the [Django tutorial](https://docs.djangoproject.com/en/1.9/intro/tutorial01/). 

1. Browse to where you want your project created on the terminal. 
2. Create your project: `django-admin startproject mysite`
3. Change into your new project directory: `cd mysite`
4. Test your new project by starting the server: `python manage.py runserver` (ignore migrations warning for now)
5. Now browse to `http://127.0.0.1:8000/` and verify you see the "It Worked!" page.

**Now let's create an app.**

1. Make sure you are in the same directory as your project's `manage.py` file (unless you want to install the app as a submodule)
2. Create the app: `python manage.py startapp my_app_name`
3. Write your first view of your app. Open up `my_app_name/views.py` and type:

    ```python
    from django.http import HttpResponse
    
    def index(request):
        return HttpResponse("Hello, world. You're at the my_app_name index.")
    ```

4. Now create the file: `my_app_name/urls.py`:

    ```python
    from django.conf.urls import url
    from . import views
    
    urlpatterns = [
        url(r'^$', views.index, name='index'),
    ]
    ```
    
5. Now register your app's urls with your project urls. In `mysite/urls.py`:

    ```python
    from django.conf.urls import include, url
    from django.contrib import admin
    
    urlpatterns = [
        url(r'^my_app_name/', include('my_app_name.urls')),
        url(r'^admin/', admin.site.urls),
    ]
    ```
    
6. Now run the server: `python manage.py runserver`
7. Browse to `http://127.0.0.1:8000/my_app_name/`
8. You should see: `Hello, world. You're at the my_app_name index.`



## Hosting 

- [Deploying Django to Heroku](https://godjango.com/4-deploying-django-to-heroku/)


## Recommended Libraries / Utilities
 
- [virtualenv](https://virtualenv.readthedocs.org/en/latest/userguide.html#usage) Wrap your Django projects in a virtualenv and shelter/control your dependencies. 






