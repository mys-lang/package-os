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

Environment variables example
=============================

An example of how to use environment variables.

.. code-block:: python

   from os import env
   from os import setenv
   from os import getenv

   def main():
       print("Before:", getenv("FOOBAR", "ho"))
       setenv("FOOBAR", "hi")
       print("After: ", getenv("FOOBAR"))

       for name in slice(env().keys(), 0, 5):
           print(name)

.. _Mys programming language: https://github.com/mys-lang/mys
