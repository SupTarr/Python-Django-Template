# Writing your first Django app

## Part 1

### Creating a project

```bash
django-admin startproject mysite
```

Let’s look at what `startproject` created:

```bash
mysite/
├── manage.py
└── mysite/
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

- The outer `mysite/` root directory is a **container** for your project.
- `manage.py`: A command-line utility that lets you interact with this Django project in various ways.
- The `inner mysite/` directory is the actual **Python package** for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. mysite.urls).
- `mysite/__init__.py`: An empty file that tells Python that this directory should be considered a **Python package**.
- `mysite/settings.py`: Settings/configuration for this Django project. Django settings will tell you all about how settings work.
- `mysite/urls.py`: The URL declarations for this Django project; a “**table of contents**” of your Django-powered site.
- `mysite/asgi.py`: An entry-point for **ASGI**-compatible web servers to serve your project.
- `mysite/wsgi.py`: An entry-point for **WSGI**-compatible web servers to serve your project.

### Creating the Polls app

```bash
python manage.py startapp polls
```

Let’s look at what `startproject` created:

```bash
polls/
├── __init__.py
├── admin.py
├── apps.py
├── models.py
├── tests.py
├── views.py
└── migrations/
    └── __init__.py
```

```python
# polls/views.py
from django.http import HttpResponse


def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")
```

```python
# polls/urls.py
from django.urls import path

from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

```python
# mysite/urls.py
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('polls/', include('polls.urls')),
    path('admin/', admin.site.urls),
]
```
