django-auth-example

## Requirements

* Python 3.7
* Django 2.2
* And others listed in requirements.txt

## Setup databases using Docker and Run application on local machine

```sh
# django
export DJ_SECRET_KEY=secretkey
export DJ_DEBUG=True

# social-auth
export SOCIAL_AUTH_GITHUB_KEY=xxxxxxxxxxxxxxxxxxxx
export SOCIAL_AUTH_GITHUB_SECRET=yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy
```

Running:

```console
$ pip -c requirements/constraints.txt install -r requirements/develop.txt
$ python manage.py migrate
$ python manage.py insert_dummy_data
$ python manage.py runserver
```

## Branch structures

* `master`: The project on master branch customizing User model, supporting Github OAuth.
* `base`: Base branch to see the changes of each Pull Requests to describe following features.
    * `email-auth-backend`: Email/Password authentication built on custom authentication backend.
    * `customize-user-model`: How to define custom user model from AbstractBaseUser.
    * `django-social-auth`: Social authentication using social-auth-core.
    * `github-oauth-from-scratch`: Social authentication from scratch (There is no dependency with social-auth-core).

# License

This software is released under the MIT License, see LICENSE.txt.
