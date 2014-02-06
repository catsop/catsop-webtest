catsop-webtest
==============

A simple Django website which uses the django-sopnet application (just like
CATMAID will do it).

Setup
=====

To set this website up, your environment needs to full-fill all dependencies
listed in the file `pip-frozen`. The easiest way is probably to use a new
`virtualenv` for this:

    mkvirtualenv --no-site-packages -p /usr/bin/python2.7 catsop-webtest

You should be in this `virtualenv` afterwards. If not, use `workon
catsop-webtest` to activate it (and `deactivate` to get out of it again).
