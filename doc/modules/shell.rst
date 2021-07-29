shell -- Shell-like commands
============================

Example
-------

Pipe output from one command to another and collect the resulting
lines.

.. note:: Maybe remove this module if/when iterators are implemented.

.. code-block:: python

   from os.shell import find
   from os.shell import Pipe

   def main():
       print(find("*").grep("x", invert=True).collect())
       print(Pipe(["b", "b", "a"]).uniq().sort().collect())

API
---

.. mysfile:: src/shell.mys
