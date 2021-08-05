tty -- Terminal control functions
=================================

Example
-------

The code:

.. code-block:: mys

   from os.tty import set_to_cbreak_mode
   from os import STDIN
   # ToDo: Should not be needed.
   from os import Stdin

   def main():
       set_to_cbreak_mode(0)

       while True:
           print(f"Got '{char(i32(STDIN.get()))}'.")

Build and run:

.. code-block:: myscon

   ❯ mys build
    ✔ Reading package configuration (0 seconds)
    ✔ Building (0.01 seconds)
   ❯ ./build/speed/app
   Got '1'.
   Got '2'.
   Got '3'.
   Got 'a'.
   Got 'b'.
   Got 'c'.

API
---

.. mysfile:: src/tty.mys
