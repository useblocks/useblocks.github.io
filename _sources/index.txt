
.. useblocks blog index file, created by `ablog start` on Wed Jul 15 19:34:12 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to useblocks team's Blog!
==========================================

Hello World! Find more about me here: :ref:`about`


Here is a list of most recent posts:

.. postlist:: 5


.. `toctree` directive, below, contains list of non-post `.rst` files.
   This is how they appear in Navigation sidebar. Note that directive
   also contains `:hidden:` option so that it is not included inside the page.

   Posts are excluded from this directive so that they aren't double listed
   in the sidebar both under Navigation and Recent Posts.

.. toctree::
   :hidden:

   about.rst

