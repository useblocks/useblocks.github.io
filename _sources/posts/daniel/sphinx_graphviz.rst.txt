.. post:: 19 Jul, 2015
   :tags: diagramme, sphinx, dot, graphviz
   :category: Tools
   :author: Daniel
   :excerpt: 1

Graphviz in Sphinx
==================
.. _Graphviz: http://www.graphviz.org
.. _Sphinx: http://www.sphinx-doc.org
.. _PlantUML: http://plantuml.com

Vor einiger Zeit habe ich `PlantUML`_ in `Sphinx`_ integriert, um schnell und einfach Diagramme zeichnen zu können.
Bei einer kleinen Recherche habe ich nun herausgefunden, dass auch `Graphviz`_ in `Sphinx`_ ohne größere Probleme
unterstützt wird.

Der Artikel über `PlantUML`_ findet man hier: :ref:`diagramme_mit_plantuml`

Vorgehen
--------
Zuerst muss `Graphviz`_ installiert werden. Unter Linux geschieht dies unter anderem über::

    sudo apt-get install graphviz


Danach muss in der `Sphinx`_ **conf.py** nur noch die Unterstützung von `Graphviz`_ aktiviert werden::

    extensions = [
    'sphinx.ext.extlinks',
    'sphinx.ext.intersphinx',
    'sphinx.ext.todo',
    'alabaster',
    'ablog',
    'sphinxcontrib.plantuml',
    'sphinx.ext.graphviz',  # Dies ist die wichtige Zeile
    ]

Ich habe die anderen Extensions aus unserer Sphinx-Config mal drin gelassen, damit für Leute, die :ref:`sphinx_blog`
gelesen haben, die Config identisch ist.

Das war's. Danach kann man auch schon mit der Benutzung starten.

Benutzung
---------

Die `Graphviz`_-Diagramme lassen sich ähnlich wie die `PlantUML`_-Diagramme integrieren.::

    .. graph:: foo
    "Peter" -- "Hans";

die führt zu

.. graph:: foo

    "Peter" -- "Hans";

Die Dokumentation über die Sphinx-Erweiterung **sphinx.ext.graphviz** ist hier zu finden:
http://sphinx-doc.org/ext/graphviz.html

`Graphviz`_ ist um einiges mächtiger als `PlantUML`_. Dadurch allerdings auch nicht so einfach zu benutzen bzw. die
Benutzung für UML-Diagrammen kommt dort an ihre Grenzen.

Einen umfangreichen Artikel über die Möglichkeiten mit `Graphviz`_ ist z.B. http://4webmaster.de/wiki/Graphviz-Tutorial

Die offiziellen Referenzen zur Sprache sind hier abgelegt: http://www.graphviz.org/Documentation.php
