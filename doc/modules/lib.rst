os -- OS utilities
==================

This modules provides various functions adn types that are close to
the operating system.

Files and folders example
-------------------------

.. code-block:: mys

   from os import cd
   from os import cwd
   from os import exists
   from os import mkdir
   from os import rm
   from os import touch
   from os import which

   def main():
       try:
           path = which("ls")
           print(f"executable ls found at '{path}'")
       except OsError:
           pass

       mkdir("foo")
       cd("foo")
       print("Current working directory is", cwd())
       touch("bar")

       if exists("bar"):
           print("bar exists")

       cd("..")
       rm("foo", recursive=True, force=True)

Environment variables example
-----------------------------

An example of how to use environment variables.

.. code-block:: mys

   from os import env
   from os import setenv
   from os import getenv

   def main():
       print("Before:", getenv("FOOBAR", "ho"))
       setenv("FOOBAR", "hi")
       print("After: ", getenv("FOOBAR"))

       for name in slice(env().keys(), 0, 5):
           print(name)

API
---

.. mysfile:: src/lib.mys
