# :memo: Notes
## DJANGO
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Django](https://www.djangoproject.com/)
- [Django documentation](https://docs.djangoproject.com/)
- [Topics](https://docs.djangoproject.com/en/4.2/topics/)
- [API Reference](https://docs.djangoproject.com/en/4.2/ref/)
- [“How-to” guides](https://docs.djangoproject.com/en/4.2/howto/)
- [django-admin and manage.py](https://docs.djangoproject.com/en/4.2/ref/django-admin/)
- [Classy Class-Based Views](https://ccbv.co.uk/)
- [Design philosophies](https://docs.djangoproject.com/en/4.2/misc/design-philosophies/)
- [Django Debug Toolbar](https://django-debug-toolbar.readthedocs.io/)
### Requirements
- [Python](https://www.python.org/)
### Terms and concepts
* Django Architecture MVT (Model-View-Template)
  - Model: the data layer
  - View: the logic layer
  - Template: the presentation layer

* Flow
  - URL
  - View
  - Model
  - Template

* Model Layer
  - To structure and interact with applicaton's data.
  - The blueprint for data.
  - It is the single, definitive source of truth for information.

* View Layer
  - Is the "business logic" of application.
  - It's the thinker and the decision-maker.
  - It's the middleman that connects the Models and the Template.

* Template Layer
  - HTML that defines the structure and content of a page.
  - It's responsible for presentation.
  - It separates the look of the page from the Python logic.

- Template Engine combine the templates with the data to generate a final HTML page.

* Forms

---

* Database
  - Table
  - Column
  - Key
  - Relationship
- ORM (Object-Relational Mapper) (Object-Relational Mapping)
- Python
- Python package
- Python web framework
- Installation
- Project container
* Project
  - django-admin
  - manage.py
  - settings.py
  - urls.py
- Development server
* Application
  - include the app in the project, add application in settings.py file
- Views
* Urls
  - include
  - path
* Database
  - settings.py
  - migrate
* All the common database relationships
  - many-to-one
  - many-to-many
  - one-to-one
* Models
  - Activating models
  - makemigrations
  - migrate
- Admin user or Super user
- Administrative interface
* Public interface "view"
  - URL dispatcher
  - template
  - namespace
- Templates
- Forms
- Tests
- Styles
- Debug Toolbar

#### Django Site Administration
* Authentication and Authorization
  - Groups
  - Users

* The Three Key Models
  - User
  - Permission
  - Group

- Create Groups
- Assign Users to a Group
- Specific Permission

is_staff

Pro tip: Check for permissions, not group names
### Setup
Verifying  
To verify that Django can be seen by Python, type python from your shell. Then at the Python prompt, try to import Django:
```
>>> import django
>>> print(django.get_version())
4.2
```
Or you can tell Django is installed and which version by running the following command in a shell prompt:
```
$ python -m django --version
```
#### Create a Django project in virtual environment
Create virtual environment
```
$ python -m venv <name>
```
Activate virtual environment
```
$ source <name>/bin/activate
```
Deactivate virtual environment
```
$ deactivate
```
Install Django
```
$ pip install django
```
```
$ python -m pip install Django
```
Verifying
```
$ python3 -m django --version
```
Creating a project
```
$ django-admin startproject <name> .
```
Interactive Python shell
```
$ python manage.py shell
```
Creating an application
```
$ django-admin startapp <name>
```
Sync database
```
$ python manage.py migrate
```
Create super user
```
$ python manage.py createsuperuser
```
Run server
```
$ python manage.py runserver
```
#### Create a Django project in Docker
docker-compose.yml file
```
services:
  web:
    build: .
    command: python manage.py runserver 0.0.0.0:8000
    volumes:
      - .:/src
    ports:
      - '8000:8000'
```
Dockerfile file
```
FROM python:3.11
ENV PYTHONUNBUFFERED 1
RUN mkdir /src
WORKDIR /src
COPY requirements.txt /src/
RUN python -m pip install -r requirements.txt
COPY . /src/
```
requirements.txt file
```
Django==4.1
```
Create project
```
$ docker-compose run web django-admin startproject <project_name> .
```
Change the ownership of the new files
```
$ chown -R $USER:$USER web manage.py
```
Apply the migrations
```
$ docker-compose run web python manage.py migrate
```
Create super user
```
$ docker-compose run web python manage.py createsuperuser
```
Run
```
$ docker-compose up
```
Done!
- http://127.0.0.1:8000/
- http://127.0.0.1:8000/admin/
Run bash
```
$ docker exec -it <container> bash
```
#### New Packages
From project root, with venv activated
##### pyproject file
Generate/update pyproject.toml in project root
```
$ python scripts/generate_pyproject.py
```
Custom name and version
```
$ python scripts/generate_pyproject.py --name o_p-web-app --version 0.1.0
```
Preview without writing
```
$ python scripts/generate_pyproject.py --dry-run
```

```
$ pip install -e .
```
##### requirements file
```
$ pip freeze > requirements.txt
```

```
$ pip install -r requirements.txt
```
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2023 - 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
