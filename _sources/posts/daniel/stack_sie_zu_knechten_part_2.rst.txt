.. post::
   :tags: alt, neu, turn_over
   :category: Life
   :author: Daniel
   :excerpt: 1

Teil 2: Stand der Dinge
=======================

Dieser Teil der Serie befasst sich mit den aktuell verwendeten Technologien und Libraries sowie mit der SW-Architektur selbst. Am Ende werden die Probleme genauer erörtert, die wir mit dem aktuellen Stand haben.

Die anderen Teile im Überblick:
Teil 1: Alles doof! Alles neu!

Teil 2: Stand der Dinge

Teil 3: Wunschkonzert

Teil 4: Entwicklungsschritte

Teil 5: SW-Stack

groundwork wurde mit Python, Javascript, CSS und HTML entwickelt. Wobei Python im Backend und der Rest rein im Frontend verwendet wird.

Um das Rad nicht neu zu erfinden und die notwendigen Wartungsarbeiten gering zu halten, setzen wir auf eine Reihe von Open-Source-Projekten, die während der Installation automatisch angezogen werden. Wir arbeiten eher in diesen Projekten mit, als dass wir sie forken. Dadurch ist gewährleistet, dass unser Framework von zukünftigen Entwicklungen profitiert und wir diese nicht selbst nachpflegen müssen.

Für das Backend setzen wir unter anderem auf folgende Libraries:

* Yapsy: Plugin-Framework
* Flask: Micro-Webframework
* Flask-Security: User und Role-Management
* SQLAlchemey:  SQL-Wrapper für verschiedene, relationale Datenbanken (MySQL, sqlite, Oracle SQL, MS SQL, PostgreSQL)
* Flask-Bable: Multi-language Support
* Sphinx: Automatische User-Dokumentation
* unittest: Unit-Tests inkl. Code-Coverage und Test-Reports
* Swagger-UI: Automatische, interaktive REST-API Dokumentation
* Jinja: HTML-Template Engine

Unser Hauptaufgabe ist es, all die unterschiedlichen Bibliotheken über eine gemeinsame und einfache Programmierschnittstellen dem Ingenieur zur Verfügung zu stellen. Wir haben dies dann erreicht, wenn er gar nicht merkt, mit welchen Bibliotheken er gerade arbeitet.

Der letzte Punkt in der Lib-Liste hat es verraten, wir erzeugen momentan unseren HTML-Code komplett serverseitig. Dynamische Frontend-Anteile sind eher selten und werden dann über jQuery realisiert. Somit enthalten Plugins in groundwork neben Datenbank-Modellen, Business-Logik und APIs auch die Views fürs Frontend.

Diese Backend-Frontend-Kopplung im Plugin führt über längere Zeit zu ein paar Problemen:

Die Views verwenden selten die Plugin-REST-API und beziehen ihre Daten direkt über Datenbank-Abfragen. Dadurch wurde die REST-API meistens nur notdürftig entwickelt.
Die Plugin-Views legen die Funktion gegenüber dem Nutzer fest. Alternative Views durch andere Plugins sind eher schwierig, da auf die REST-API nicht zuverlässig zurückgegriffen werden kann.
Das Datenbank-Schema kann nur schwer geändert werden, da zahlreiche Plugins ein bestimmtes Schema für ihre Views erwarten. Eine einfache Abstraktion über eine REST API gibt es nicht.
Da der HTML-Code serverseitig generiert wird, steht es jedem Plugin frei eigene Javascript-Bibliotheken anzuziehen und zu verwenden.