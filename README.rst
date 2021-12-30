pprint3x
========


Version v3.10.1 as of 2021-12-30 see `Changelog`_

|build_badge| |license| |jupyter| |pypi| |black|

|codecov| |better_code| |cc_maintain| |cc_issues| |cc_coverage| |snyk|



.. |build_badge| image:: https://github.com/bitranox/pprint3x/actions/workflows/python-package.yml/badge.svg
   :target: https://github.com/bitranox/pprint3x/actions/workflows/python-package.yml


.. |license| image:: https://img.shields.io/github/license/webcomics/pywine.svg
   :target: http://en.wikipedia.org/wiki/MIT_License

.. |jupyter| image:: https://mybinder.org/badge_logo.svg
   :target: https://mybinder.org/v2/gh/bitranox/pprint3x/master?filepath=pprint3x.ipynb

.. for the pypi status link note the dashes, not the underscore !
.. |pypi| image:: https://img.shields.io/pypi/status/pprint3x?label=PyPI%20Package
   :target: https://badge.fury.io/py/pprint3x

.. |codecov| image:: https://img.shields.io/codecov/c/github/bitranox/pprint3x
   :target: https://codecov.io/gh/bitranox/pprint3x

.. |better_code| image:: https://bettercodehub.com/edge/badge/bitranox/pprint3x?branch=master
   :target: https://bettercodehub.com/results/bitranox/pprint3x

.. |cc_maintain| image:: https://img.shields.io/codeclimate/maintainability-percentage/bitranox/pprint3x?label=CC%20maintainability
   :target: https://codeclimate.com/github/bitranox/pprint3x/maintainability
   :alt: Maintainability

.. |cc_issues| image:: https://img.shields.io/codeclimate/issues/bitranox/pprint3x?label=CC%20issues
   :target: https://codeclimate.com/github/bitranox/pprint3x/maintainability
   :alt: Maintainability

.. |cc_coverage| image:: https://img.shields.io/codeclimate/coverage/bitranox/pprint3x?label=CC%20coverage
   :target: https://codeclimate.com/github/bitranox/pprint3x/test_coverage
   :alt: Code Coverage

.. |snyk| image:: https://img.shields.io/snyk/vulnerabilities/github/bitranox/pprint3x
   :target: https://snyk.io/test/github/bitranox/pprint3x

.. |black| image:: https://img.shields.io/badge/code%20style-black-000000.svg
   :target: https://github.com/psf/black

backport of python3.10.1 module "pprint" for python 3.6 ... 3.10



The pertinent changes from Python 3.6 to Python 3.9 are:

* ``pprint`` can now pretty-print ``types.SimpleNamespace``.
  Contributed by Carl Bordum Hansenin Python 3.9.

* ``pprint.pp`` has been added to pretty-print objects with dictionary
  keys being sorted with their insertion order by default. Parameter
  *sort_dicts* has been added to ``pprint.pprint``, ``pprint.pformat`` and
  ``pprint.PrettyPrinter``. Contributed by Rémi Lapeyre in Python 3.8.

----

automated tests, Travis Matrix, Documentation, Badges, etc. are managed with `PizzaCutter <https://github
.com/bitranox/PizzaCutter>`_ (cookiecutter on steroids)

Python version required: 3.6.0 or newer

tested on recent linux with python 3.6, 3.7, 3.8, 3.9, 3.10.0, pypy-3.8 - architectures: amd64

`100% code coverage <https://codecov.io/gh/bitranox/pprint3x>`_, flake8 style checking ,mypy static type checking ,tested under `Linux, macOS, Windows <https://github.com/bitranox/pprint3x/actions/workflows/python-package.yml>`_, automatic daily builds and monitoring

----

- `Try it Online`_
- `Usage`_
- `Usage from Commandline`_
- `Installation and Upgrade`_
- `Requirements`_
- `Acknowledgements`_
- `Contribute`_
- `Report Issues <https://github.com/bitranox/pprint3x/blob/master/ISSUE_TEMPLATE.md>`_
- `Pull Request <https://github.com/bitranox/pprint3x/blob/master/PULL_REQUEST_TEMPLATE.md>`_
- `Code of Conduct <https://github.com/bitranox/pprint3x/blob/master/CODE_OF_CONDUCT.md>`_
- `License`_
- `Changelog`_

----

Try it Online
-------------

You might try it right away in Jupyter Notebook by using the "launch binder" badge, or click `here <https://mybinder.org/v2/gh/{{rst_include.
repository_slug}}/master?filepath=pprint3x.ipynb>`_

Usage
-----------

for documentation see : https://docs.python.org/3/library/pprint.html

and select Python Version 3.10.1

Usage from Commandline
------------------------

.. code-block::

   Usage: pprint3x [OPTIONS] COMMAND [ARGS]...

     backport of pprint from python 3.11

   Options:
     --version                     Show the version and exit.
     --traceback / --no-traceback  return traceback information on cli
     -h, --help                    Show this message and exit.

   Commands:
     info  get program informations

Installation and Upgrade
------------------------

- Before You start, its highly recommended to update pip and setup tools:


.. code-block::

    python -m pip --upgrade pip
    python -m pip --upgrade setuptools

- to install the latest release from PyPi via pip (recommended):

.. code-block::

    python -m pip install --upgrade pprint3x

- to install the latest version from github via pip:


.. code-block::

    python -m pip install --upgrade git+https://github.com/bitranox/pprint3x.git


- include it into Your requirements.txt:

.. code-block::

    # Insert following line in Your requirements.txt:
    # for the latest Release on pypi:
    pprint3x

    # for the latest development version :
    pprint3x @ git+https://github.com/bitranox/pprint3x.git

    # to install and upgrade all modules mentioned in requirements.txt:
    python -m pip install --upgrade -r /<path>/requirements.txt


- to install the latest development version from source code:

.. code-block::

    # cd ~
    $ git clone https://github.com/bitranox/pprint3x.git
    $ cd pprint3x
    python setup.py install

- via makefile:
  makefiles are a very convenient way to install. Here we can do much more,
  like installing virtual environments, clean caches and so on.

.. code-block:: shell

    # from Your shell's homedirectory:
    $ git clone https://github.com/bitranox/pprint3x.git
    $ cd pprint3x

    # to run the tests:
    $ make test

    # to install the package
    $ make install

    # to clean the package
    $ make clean

    # uninstall the package
    $ make uninstall

Requirements
------------
following modules will be automatically installed :

.. code-block:: bash

    ## Project Requirements
    click
    cli_exit_tools
    dataclasses; python_version < '3.7'
    lib_detect_testenv

Acknowledgements
----------------

- special thanks to "uncle bob" Robert C. Martin, especially for his books on "clean code" and "clean architecture"

Contribute
----------

I would love for you to fork and send me pull request for this project.
- `please Contribute <https://github.com/bitranox/pprint3x/blob/master/CONTRIBUTING.md>`_

License
-------

This software is licensed under the `MIT license <http://en.wikipedia.org/wiki/MIT_License>`_

---

Changelog
=========

- new MAJOR version for incompatible API changes,
- new MINOR version for added functionality in a backwards compatible manner
- new PATCH version for backwards compatible bug fixes

v3.10.1
--------
2021-12-30: initial release

