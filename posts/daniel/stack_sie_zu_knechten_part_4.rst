.. post:: 20 Jun, 2015
   :tags: alt, neu, turn_over
   :category: Life
   :author: Daniel
   :excerpt: 1


Teil 4: Entwicklungsschritte
============================

Im letzten Teil der Serie ging es um unsere Wünsche in Richtung Entwicklungsprozess und SW Stack. Dieser Teil befasst sich nun mit den notwendigen Entwicklungsschritten einer einzelnen Änderung.

Die anderen Teile im Überblick:

Teil 1: Alles doof! Alles neu!

Teil 2: Stand der Dinge

Teil 3: Wunschkonzert

Teil 4: Entwicklungsschritte

Teil 5: SW-Stack

Software-Struktur
-----------------

Unsere SW besteht in der Regel aus einer App, die ihre Funktionen über Plugins bezieht, die in unterschiedlichen Repositories gepflegt werden.

Diese Struktur ermöglicht es uns mehrere, unterschiedliche Apps zu haben, die sich aber einen Großteil der Funktionen/Plugins teilen.

Dank diesem Vorgehen startet eine neue App-Entwicklung niemals bei 0, sondern kann meistens 80% der notwendigen Funktionen schon von vorhandenen Plugins übernehmen.

Konzept und Spec
****************

* Konzept im Wiki darlegen und diskutieren
* Ticket erzeugen
* Spezifizierung
* Feature-Branch für das Ticket im App-Repository erzeugen
* REST-API Spezifikation schreiben/updaten
* Spezifikation in den Feature-Branch commiten
* REST-API Dokumentation wird generiert
* REST-API Tests werden generiert

Der Feature-Branch wird hier noch nicht wieder in der Master gemerged, da er noch für die Integration der Plugins benötigt wird. Erst wenn die Integrationstests fehlerfrei durchgelaufen sind, kann die Änderung endgültig auf den Master eingespielt werden.

Backend
*******

* Feature-Branch im jeweiligen Plugin-Repository erzeugen
* groundwork Plugin Skeletons basierend auf REST-API Spezifizierung generieren (optional)
* groundwork Plugins entwickeln
* Inklusive Unit Tests
* Inklusive User-Dokumentation
* Änderung auf den Feature-Branch commiten
* Unit-Tests werden durchgeführt
* Feature-Branch in den Master des Plugin-Repos mergen
* Unit-Tests werden durchgeführt
* Im Feature-Branch des App-Repository neue Plugin-Versionen anziehen/konfigurieren
* Änderungen auf den Feature-Branch commiten
* Unit-Tests werden durchgeführt
* Integrations-Tests werden durchgeführt
* User und REST-API Dokumentation werden generiert
* Feature-Branch in den Master des App-Repositorys mergen
* Unit-Tests werden durchgeführt
* Integrations-Tests werden durchgeführt
* User und REST-API Dokumentation werden generiert
* Deployment auf Test-Servern wird automatisiert vorgenommen

Frontend
********

Da die REST-API Spezifikation schon feststeht, kann die Frontend-Entwicklung gleichzeitig mit der Backend-Entwicklung starten.

* Feature-Branch im jeweiligen Plugin-Repository erzeugen
* Plugins entwickeln
* Inklusive Unit Tests
* Inklusive User-Dokumentation
* Änderung auf den Feature-Branch commiten
* Unit-Tests werden durchgeführt
* Feature-Branch in den Master des Plugin-Repos mergen
* Unit-Tests werden durchgeführt
* Im Feature-Branch des Frontend-App-Repository neue Plugin-Versionen anziehen/konfigurieren
* Änderungen auf den Feature-Branch commiten
* Unit-Tests werden durchgeführt
* Integrations-Tests werden durchgeführt
* Feature-Branch in den Master des Frontend-App-Repositorys mergen
* Unit-Tests werden durchgeführt
* Integrations-Tests werden durchgeführt
* Deployment auf Test-Servern wird automatisiert vorgenommen