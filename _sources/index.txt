
.. useblocks blog index file, created by `ablog start` on Wed Jul 15 19:34:12 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

useblocks Blog!
===============

Willkommen auf unserem Team Blog.

Hier dreht sich alles um Themen rund um SW-Entwicklung, Service-Architekturen und Unternehmensprozessen.

Wir als Team sind:

.. image:: /_static/autoren.png

Unsere letzten Beiträge
-----------------------

.. postlist:: 5
   :format: {title} von {author} am {date}
   :date: %d.%m.%Y
   :excerpts:


.. `toctree` directive, below, contains list of non-post `.rst` files.
   This is how they appear in Navigation sidebar. Note that directive
   also contains `:hidden:` option so that it is not included inside the page.

   Posts are excluded from this directive so that they aren't double listed
   in the sidebar both under Navigation and Recent Posts.

.. toctree::
   :maxdepth: 1
   :hidden:

   useblocks Blog <http://useblocks.github.io>
   useblocks Website <http://www.useblocks.com>
   datablocks Website <http://www.datablocks.de>

