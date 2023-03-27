# Python Django Template

## About The Project

This project was completed as part of `Writing your first Django app,` form `Django documentation`. I am tasked to make full use of our Django and Python knowledge and its accompanying documentation to create a APIs for polls and vote.

## Technologies

This project was created with:

- Python
- Django
- PostgreSQL

## Installation

### Set up Python

To install `Python` on your machine go to [Python Download](https://www.python.org/downloads/).

```cmd
py --version
```

To install `virtualenv` via pip

```cmd
py -m pip install --user virtualenv
```

To create a `virtual environment` for your project, open a new command prompt, navigate to the folder where you want to create your project and then enter the following:

```cmd
py -m virtualenv .
```

To activate the environment, run:

```cmd
.\Scripts\activate.bat
```

In the command prompt, ensure your virtual environment is active, and execute the following command:

```cmd
py -m pip install Django
```

Output installed packages in `requirements` format.

```cmd
pip3 freeze > requirements.txt
```

Create a `mysite` directory in your current directory.

```cmd
django-admin startproject mysite
```

To create your app, make sure you’re in the same directory as `manage.py` and type this command:

```cmd
py manage.py startapp app_name
```

Verify it’s working with the following command:

```cmd
python manage.py runserver
```
