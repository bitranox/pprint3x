.. start short_desc

Backport of pprint from Python 3.10.1 to Python 3.7-3.9**

.. end short_desc

The pertinent changes from Python 3.7 to Python 3.9 are:

* ``pprint`` can now pretty-print ``types.SimpleNamespace``.
  Contributed by Carl Bordum Hansenin Python 3.9.

* ``pprint.pp`` has been added to pretty-print objects with dictionary
  keys being sorted with their insertion order by default. Parameter
  *sort_dicts* has been added to ``pprint.pprint``, ``pprint.pformat`` and
  ``pprint.PrettyPrinter``. Contributed by Rémi Lapeyre in Python 3.8.
