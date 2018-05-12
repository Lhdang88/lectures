## Microservices

* modernes / populäres Architekturmuster in der Cloud
* eignen sich für "App-Containerisierung"
* eignen sich für die horizontale Skalierung in der Cloud
* eignen sich für "Continous Delivery"

down:

### Philosophie

* Entkopplung von Funktionalitäten in kleine eigenständig lebende Funktionen
* Dekomposition von Applikationen in abgegrenzte, isolierte Module
* Überschaubarkeit, Einfachkeit von Komponenten
* Offene Schnittstellen, keine proprietäre Protokolle, meistens Http + JSON/XML
* Programmiersprachenunabhängigkeit von Komponenten
* Entkopplung von Entwicklungsteams

down:

### Vorteile

* unabhängige Skalierbarkeit von Microservices
* bessere Wartbarkeit, einfache Neuimplementierung
* versteckte Abhängigkeiten werden über die API erkennbar
* Sprachenunabhängig, Teams können nach ihren Wünschen den Technologiestack auswählen
* unabhängige Entwicklungszyklen, Parallelisierung der Entwicklung
* bei Überlastung (DDos) können sekundäre Services zugunsten von primären Services abgeschaltet werden

down:

### Nachteile

* Performance Overhead durch Netzwerk-Kommunikation
* Erhöhte Komplexität von Tests: Unit/Komponenten-Tests werden Integrationstests
* Erhöhte Komplexität von Monitoring: zentralisiertes Monitoring, Splunk, AppDynamics etc.
* Deployment Prozess muss ggfs. zwischen Teams abgestimmt werden (API Breaking Changes)
* Einführung von generellen Problemen von verteilten Anwendungen: z.B. Lastverteilung, Zeitsynchronisation, distributed Locking

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/CKL3fV5UR8w" frameborder="0" allowfullscreen></iframe>

https://www.youtube.com/embed/CKL3fV5UR8w

down:

## 12-Factor Apps

<img src="media/12factor.png"/>

* [Wikipedia](https://en.wikipedia.org/wiki/Twelve-Factor_App_methodology)

down:

#### Diskussion

Was ist der Sinn und Zweck von 12 Factor Apps

* 15 min.
