.. post:: 19 Jun, 2015
   :tags: alt, neu, turn_over
   :category: Life
   :author: Daniel
   :excerpt: 2

Teil 3: Wunschkonzert
=====================
Quo vadis? Wie soll's weitergehen?

Dieser Teil aus der Serie über unseren SW-Stack bei useblocks befass sich mit den Wünschen, die wir für den SW-Stack aber auch für unseren Entwicklungsprozess haben.

Die anderen Teile im Überblick:

Teil 1: Alles doof! Alles neu!

Teil 2: Stand der Dinge

Teil 3: Wunschkonzert

Teil 4: Entwicklungsschritte

Teil 5: SW-Stack

Aufgrund der Probleme ahnt man schon, was wir uns am meisten wünschen:
Eine saubere Trennung von Backend und Frontend.

Den Plugin-basierten Ansatz von groundwork würden wir gerne auch für die Frontend-Entwicklung übernehmen. Des Weiteren wollen wir in der Lage sein, die Plugin-Tests fürs Frontend automatisch und gemeinschaftlich ausführen zu können sowie eine gemeinsame Dokumentation zu generieren.

Und um die REST-APIs mehr zu fokussieren, würden wir gerne einen API-first Ansatz in unseren Entwicklungsprozess einbauen.

Auf der Backenend-Seite würde wir gerne in der Lage sein, aus einer API-Spezifikation automatisch Plugins und Tests für groundwork generieren zu können sowie die von einer Webapp bereitgestellte REST-API gegen eine Spezifizierung zu testen.

Was noch fehlt ist natürlich eine funktionierende Umsetzung von Continuous Integration und Delivery, so dass jede Code-Änderung automatisch getestet und bei Bestehen auf Test-Servern ausgerollt wird. Ach ja, Qualitäts-Metriken sollen natürlich auch direkt erhoben werden (Performance, Antwortzeiten, Speicherverbrauch, ...)

Da wir bis jetzt meistens eher in einem ristriktiven B2B-Umfeld unterwegs waren, hatten wir nicht die Möglichkeit auf die zahlreichen Cloud-Angebot rund um die SW-Entwicklung zurückzugreifen. Dies soll sich mit der Veröffentlichung von groundwork ändern, so dass wir versuchen möglichst viele Platzhirsche auf ihren jeweiligen Fachgebieten in unseren SW-Stack zu integrieren.