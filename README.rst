planet.sympy.org
================

This repository hosts http://planet.sympy.org/.
The contents of it is generated and pushed into automatically.

Installation
------------

On Ubuntu::

    sudo apt-get install planet-venus

Build (or update) the planet::

    ./update

Developer Information
---------------------

The ``common`` directory is copied from ``/usr/share/planet-venus/theme/`` and
``theme`` is copied from ``/usr/share/planet-venus/theme/classic_fancy``.
SymPy logo was added into the ``theme/images``. If you want to modify the
contens of the main planet page, just modify the file
``theme/index.html.tmpl``.
