
.. useblocks blog index file, created by `ablog start` on Wed Jul 15 19:34:12 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

useblocks Blog
==============

Willkommen auf unserem Team Blog.

Hier dreht sich alles um Themen rund um SW-Entwicklung, Hardware/Embedded, Architekturen und Unternehmensprozesse.

Wir als Team sind:

.. image:: /_static/autoren.png

|

Unsere letzten Beiträge
=======================

.. postlist:: 20
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

   ub Präsentationen <http://useblocks.github.io/presentations>
   ub Website <http://www.useblocks.com>
