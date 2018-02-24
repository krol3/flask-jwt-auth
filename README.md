# Flask JWT Auth

Origin from: https://realpython.com/blog/python/token-based-authentication-with-flask/

[![Build Status](https://travis-ci.org/realpython/flask-jwt-auth.svg?branch=master)](https://travis-ci.org/realpython/flask-jwt-auth)
https://github.com/realpython/flask-jwt-auth

## Quick Start

### Basics

1. Activate a virtualenv
```
$ virtualenv --python=/usr/bin/python3.6 venv
$ source venv/bin/activate
```

1. Install the requirements
```
pip install -r requirements.txt
```

### Set Environment Variables

Update *project/server/config.py*, and then run:

```sh
$ export APP_SETTINGS="project.server.config.DevelopmentConfig"
```

or

```sh
$ export APP_SETTINGS="project.server.config.ProductionConfig"
```

### Create DB

Create the databases in `psql`:

```sh
sudo -u postgres psql

$ psql
# create database flask_jwt_auth
# create database flask_jwt_auth_test
# \q
```

Create the tables and run the migrations:

```sh
$ python manage.py create_db
$ python manage.py db init
$ python manage.py db migrate
```

### Run the Application

```sh
$ python manage.py runserver
```

So access the application at the address [http://localhost:5000/](http://localhost:5000/)

> Want to specify a different port?

> ```sh
> $ python manage.py runserver -h 0.0.0.0 -p 8080
> ```

### Testing

Without coverage:

```sh
$ python manage.py test
```

With coverage:

```sh
$ python manage.py cov
```

## Settings psycopg2

sudo apt-get install postgresql
sudo apt-get install python-psycopg2
sudo apt-get install libpq-dev

pip install psycopg2
pip freeze > requirements.txt

## Apply the migration
(env)$ python manage.py create_db
(env)$ python manage.py db init
(env)$ python manage.py db migrate