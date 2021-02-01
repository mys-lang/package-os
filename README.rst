Os
==

OS utilities in the `Mys programming language`_.

Basic example
=============

.. code-block:: python

   from os import which

   def main():
       if which("ls"):
           print("executable ls found")

Shell example
=============

Pipe output from one command to another and collect the resulting
lines.

Maybe remove this module if/when iterators are implemented.

.. code-block:: python

   from os.shell import find
   from os.shell import Pipe

   def main():
       print(find("*").grep("x", invert=True).collect())
       print(Pipe(["b", "b", "a"]).uniq().sort().collect())

.. _Mys programming language: https://github.com/mys-lang/mys
