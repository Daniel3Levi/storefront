Shell commend for creating new python(Django)project (Macintosh)

Start with:

pipenv install django
Do this commend in project folder

Create a Pipefile & Pipefile.lock - like json&json lock in Node js
Or like a manifest file in android

Pipenv is both a package and virtual environment management tool that uses the Pipfile and Pipfile.lock files to achieve these goals.
Pipenv handles the virtual environment for you (no more activate and deactivate required).
some basics to get started, see more at pipenv website.

—————————————————-

Need to install python interpreter inside VScode for this project only and not using the one that install globally in my Macintosh
(Should understand why later

pipenv shell
Do this commend in project folder
Output:
Launching subshell in virtual environment…(???)

—————————————————-

To see all the terminal commends that I can do in django run this utility that come with django:

django-admin

—————————————————-
To start the project type in terminal:

django-admin startproject [project-name]
This commend will create a project folder with a core folder that have a several python files:

[project core folders name]:
**init**.py - defined this directory as a package
settings.py (module) - defined the application settings
urls.py (module) - defined the application urls
asgi.py , wssgi.py - (module) used for deployment

—————————————————-

manage.py - take the settings of this project into account;
I think right now that it's like an index.html file that configure where to start running the server from.

python manage.py runserver [port-number] (optional - write explicitly when port 8000 occupied by another app)

runserver (one of the django-admin commends)

ERROR:
danielevi@Daniels-MBP-2 storefront % python manage.py runserver  
zsh: command not found: python

Solution:
Make sure you properly did the source bin/activate command. If you skip that, or do it in a different terminal window, or close the window then re-open it, you won't be in the virtualenv and you won't have access to the django-admin.py command in your environment.

Optional solution:
Try to run this command instead.
python ./manage.py runserver
