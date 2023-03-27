# Set up Django

To install Python on your machine go to [Python Download](https://www.python.org/downloads/).

```cmd
py --version
```

To install virtualenv via pip

```cmd
py -m pip install --user virtualenv
```

To create a virtual environment for your project, open a new command prompt, navigate to the folder where you want to create your project and then enter the following:

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

```cmd
pip3 freeze > requirements.txt
```
