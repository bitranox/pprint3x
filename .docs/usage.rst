to be compatible with the builtin module, just import pprint3x as follows:

.. code-block:: python

    >>> from pprint3x import pprint
    >>> pprint('test')
    'test'


or, if You need the full scope of the pprint namespace :

.. code-block:: python

    >>> import pprint3x as pprint
    >>> pprint.pprint('test')
    'test'
    >>> pprint.isreadable('test')
    True


for documentation of pprint itself, see : https://docs.python.org/3/library/pprint.html
(select Python Version 3.10.1)
