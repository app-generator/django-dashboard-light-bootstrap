# [Django Dashboard - Light Bootstrap](https://appseed.us/admin-dashboards/django-dashboard-light)

> Admin dashboard coded in **Flask** Framework with basic modules, database, ORM and deployment scripts. 

<br />

**Light Bootstrap Dashboard** is Bootstrap 4 admin dashboard template designed to be beautiful and simple. It is built on top of Bootstrap 4 and it is fully responsive. It comes with a big colections of elements that will offer you multiple possibilities to create the app that best fits your needs. It can be used to create admin panels, project management systems, web applications backend, CMS or CRM.

<br />

**Codebase Features**

- Reference Codebase - [Boilerplate Code - Django Dashboard](https://appseed.us/boilerplate-code/django-dashboard) 
- UI-Ready app, SQLite Database, Django Native ORM
- Modular design, best practices codebase
- Session-Based Authentication, Forms validation
- Deployment scripts: Docker, Gunicorn/Nginx
- Support via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup) - 24/7 LIVE Service.

> Links

- [Django Light Bootstrap](https://appseed.us/admin-dashboards/django-dashboard-light) - Official product page
- [Django Light Bootstrap Demo](https://django-dashboard-light-bootstrap.appseed.us/) - LIVE app deployment
- [Django Light Bootstrap Docs](https://docs.appseed.us/admin-dashboards/django-dashboard-light/) - Official documentation
- [Light Bootstrap Dashboard Design](https://demos.creative-tim.com/light-bootstrap-dashboard/documentation/tutorial-components.html) - Official documentation

<br />

## Want more? Go PRO!

PRO versions include **Premium UI Kits**, Lifetime updates and **24/7 LIVE Support** (via [Discord](https://discord.gg/fZC6hup))

| [Django Gradient PRO](https://appseed.us/admin-dashboards/django-dashboard-gradient-pro) | [Django Dashboard Black PRO](https://appseed.us/admin-dashboards/django-dashboard-black-pro) | [Django Dashboard Argon PRO](https://appseed.us/admin-dashboards/django-dashboard-argon-pro) |
| --- | --- | --- |
| [![Django Gradient PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-gradient-pro/master/media/django-dashboard-gradient-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-gradient-pro) | [![Django Dashboard Black PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-black-pro/master/media/django-dashboard-black-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-black-pro) | [![Django Dashboard Argon PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-argon-pro/master/media/django-dashboard-argon-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-argon-pro)

<br />
<br />

![Django Dashboard - Light Bootstrap - Template project provided by AppSeed.](https://raw.githubusercontent.com/app-generator/django-dashboard-light-bootstrap/master/media/django-dashboard-light-bootstrap-screen.png)

<br />

## How to use it

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-dashboard-light-bootstrap.git
$ cd django-dashboard-light-bootstrap
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install modules - SQLite Storage
$ pip3 install -r requirements.txt
$
$ # Create tables
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

<br />

## Code-base structure

The project is coded using a simple and intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app logic and serve the static assets
   |    |-- settings.py                    # Django app bootstrapper
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- sidebar.html         # Sidebar component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                  # Master pages
   |         |    |-- base-fullscreen.html # Used by Authentication pages
   |         |    |-- base.html            # Used by common pages
   |         |
   |         |-- accounts/                 # Authentication pages
   |         |    |-- login.html           # Login page
   |         |    |-- register.html        # Register page
   |         |
   |      index.html                       # The default page
   |     page-404.html                     # Error 404 page
   |     page-500.html                     # Error 404 page
   |       *.html                          # All other HTML pages
   |
   |-- authentication/                     # Handles auth routes (login and register)
   |    |
   |    |-- urls.py                        # Define authentication routes  
   |    |-- views.py                       # Handles login and registration  
   |    |-- forms.py                       # Define auth forms  
   |
   |-- app/                                # A simple app that serve HTML files
   |    |
   |    |-- views.py                       # Serve HTML pages for authenticated users
   |    |-- urls.py                        # Define some super simple routes  
   |
   |-- requirements.txt                    # Development modules - SQLite storage
   |
   |-- .env                                # Inject Configuration via Environment
   |-- manage.py                           # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

> The bootstrap flow

- Django bootstrapper `manage.py` uses `core/settings.py` as the main configuration file
- `core/settings.py` loads the app magic from `.env` file
- Redirect the guest users to Login page
- Unlock the pages served by *app* node for authenticated users

<br />

## Deployment

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/django-dashboard-light-bootstrap.git
$ cd django-dashboard-light-bootstrap
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running.

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind=0.0.0.0:8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.


<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## Credits & Links

- [Django](https://www.djangoproject.com/) - The official website
- [Boilerplate Code](https://appseed.us/boilerplate-code) - Index provided by **AppSeed**
- [Boilerplate Code](https://github.com/app-generator/boilerplate-code) - Index published on Github

<br />

---
[Django Dashboard - Light Bootstrap](https://appseed.us/admin-dashboards/django-dashboard-light) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).
