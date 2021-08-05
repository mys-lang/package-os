tty -- Terminal control functions
=================================

Example
-------

.. code-block:: mys

   from os.tty import set_to_cbreak_mode
   from os import STDIN

   def main():
       set_to_cbreak_mode(0)

       while True:
           print(f"Got {STDIN.get()}.")

API
---

.. mysfile:: src/tty.mys
