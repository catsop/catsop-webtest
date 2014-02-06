catsop-webtest
==============

A simple Django website which uses the django-sopnet application (just like
CATMAID will do it).

Setup
=====

Dependencies
------------

To set this website up, your environment needs to full-fill all dependencies
listed in the file `pip-frozen`. The easiest way is probably to use a new
`virtualenv` for this:

    mkvirtualenv --no-site-packages -p /usr/bin/python2.7 catsop-webtest

You should be in this `virtualenv` afterwards. If not, use `workon
catsop-webtest` to activate it (and `deactivate` to get out of it again).

Now you can satisfy all dependencies with the help of `pip`:

    pip install -r pip-frozen

Configuration file
------------------

Copy the example configuration file and adjust it to your needs:

    cp catsop/catsop/settings.py.example catsop/catsop/settings.py

At least a `SECRET_KEY` has to be generated. How this is done, is shown in the
corresponding comment in the settings file.

By default a SQLite 3 databse is used, but this can of course be adjusted as
well.

Initialization
--------------

The database in use has to be initialized. Make sure to be in the `virtualenv`
and run:

    python catsop/manage.py syncdb

If asked whether you want to create a super-user, choose `yes`.
