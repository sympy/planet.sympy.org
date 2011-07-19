planet.sympy.org
================

This repository hosts http://planet.sympy.org/.

Installation
------------

Run the ``server_update`` script (edit it first, so that it pushes into the right repository, and setup the ssh keys).
Then add it to a cron job, see the comments in the script for detailed documentation.

How it Works
------------

``planet.sympy.org`` is served by the ``gh-pages`` branch in the github
repository at: https://github.com/sympy/planet.sympy.org/

Whatever is in the ``gh-pages`` branch will appear at ``planet.sympy.org``.

The ``./update`` script generates the website and creates a new commit in the
``gh-pages`` branch (you need to have it checked out, and be in the ``master``
branch when you run it). Then you just need to push the ``gh-pages`` branch
into github.

You can run the ``./update`` script (and push the result back) manually, or you
can setup a cron job at your server and run (+push) it automatically (see the
``server_update`` script and the documentation in there how to set it up on
your server). In either case, don't forget to always pull latest changes into
the ``master`` branch first, so that you get the latest updates of the
configuration, and you don't push in some older version by accident.

How to Update Manually
----------------------

You only need this if you want to test that things work. You should always do
that if you change the configuration.

In Ubuntu::

    sudo apt-get install planet-venus

Build (or update) the planet::

    ./update

Add/Remove Subscriptions
------------------------

Add remove people from the ``Subscription`` section of the ``planet.ini`` file.

Developer Information
---------------------

The ``common`` directory is copied from ``/usr/share/planet-venus/theme/`` and
``theme`` is copied from ``/usr/share/planet-venus/theme/classic_fancy``.
SymPy logo was added into the ``theme/images``. If you want to modify the
contens of the main planet page, just modify the file
``theme/index.html.tmpl``.
