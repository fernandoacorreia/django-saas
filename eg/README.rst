===========================
Django SaaS Example Website
===========================

Introduction
============

This is a small Django project that demonstrates basic utilization of the
Django SaaS application.

Configuration
=============

Pinax
-----

This example is based on Pinax_. This choice was made for several reasons:

* Pinax gives a head start to create Django websites.
* It demonstrates good practices.
* This way the compatibility of Django SaaS with Pinax will be assured.

So the first step is to download Pinax.

For instance::

    mkdir ~/opt/
    cd ~/opt/
    svn co http://svn.pinaxproject.com/pinax/trunk pinax-edge

This example website was based on revision 1197 of the Pinax repository.
If you download a later release there may be some incompatibility.

.. _Pinax: http://pinaxproject.com/

local_settings
--------------

Inside django-saas' "eg" directory, create a file named "local_settings.py"
from the supplied example::

    cp local_settings_example.py local_settings.py

Edit local_settings.py and alter PINAX_ROOT to the absolute path where you
downloaded Pinax. Also, change ADMINS and CONTACT_EMAIL to your own data.

Database
--------

By default a sqlite3 database named dev.db will be created in the current
directory. Just create it, create an administrator user when asked, and after
that start the server::

    ./manage.py syncdb
    ...
    ./manage.py runserver
