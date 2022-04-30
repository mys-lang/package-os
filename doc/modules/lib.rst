os -- OS utilities
==================

This modules provides various functions adn types that are close to
the operating system.

Files and folders example
-------------------------

.. code-block:: mys

   from os import cwd
   from os import which
   from os.path import Path

   def main():
       if which("ls") is not None:
           print("executable ls found")

       foo = Path("foo")
       foo.mkdir()
       foo.cd()
       print("Current working directory is", cwd())
       bar = Path("bar")
       bar.touch()

       if bar.exists():
           print("bar exists")

       print(f"Files:", Path(".").ls())
       Path("..").cd()
       foo.rm(recursive=True, force=True)

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
