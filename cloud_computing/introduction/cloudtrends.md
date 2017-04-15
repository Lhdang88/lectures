## Container

Was sind Container?

* Virtuelle Laufzeitumgebung (Container) die auf einem Betriebssystem (Host) laufen
* Container vs Virtuelle Maschine (Betriebssystem Virtualisierung vs Systemvirtualisierung)
* Isolierte Laufzeitumgebung
* virtualisierte Netzwerkumgebung
* Isolierter Festplattenspeicher

note: Frage - was sind die Vorteile von Virtuellen Maschinen ? Benutzt es jemand ?

down:

* Vorteile:
 * effizient (geringerer Speicherverbrauch, gemeinsame Nutzung von Host-Bibliotheken (Linux Kernel))
 * Prozess-Isolation
 * Schnelles Laden der Laufzeitumgebung

* Nachteile:
 * Läuft mit demselben Kernel-Versionen des Hosts -> Windows-Host kann kein Linux-Container erzeugen

note: Boot2Docker ermöglicht es Unter Windows Linux Container zu erstellen

down:

Bedeutung für Cloud Computing

* Bietet Isolierte Laufzeitumgebungen für Anwendungen (Apps, Datenbanken, Message Queues etc.)
* Einsatz als konsequente Folge der effizienteren Auslastung der Resourcen im Vgl. zu VMs (Bspw. Cloud Foundry, Kubernetes)
* Schnellere Verfügbarkeit bringt Vorteile für Application-Level Skalierung (PaaS) bzw. auch für Lambda-Funktionen (Serverless)

Beispiel: Docker

down:

## Container Orchestrierung

* Frameworks die es ermöglichen verschiedene Container in einem Netzwerk zu verbinden
* Container können in dem isolierten Netzwerk miteinander Kommunizieren (App-Container mit DB-Container)
* Container können von einem Container Host transparent zu einem anderen wandern
* Horizontale Skalierung von Container - das Framework überwacht die Last einzelner Container und skaliert auf Wunsch automatisch

down:

Bedeutung für die Cloud

* Container Frameworks sind ein mächtiges Werkzeug um effizient Systeme auf Applikations/Service-Ebene aufzusetzen und zu betreiben.
* Flexibler als die Standard Werkzeuge von Cloud-Anbietern.
* Kein Vendor Lock-in, man kann mit dem Framework auf eine andere Platform migrieren
* CaaS als Alternative zur PaaS.

Beispiel: Kubernetes, Docker Swarm

down:

## Serverless

* Serverless != Ohne Server
* Cloud-Service um kurzlebige Funktionen in der Cloud zu betreiben
* In Serverless-Funktionen können On-Demand Rechenoperationen aufgerufen werden, die nicht ständig laufen müssen
* Lambda-Funktionen werden On-Demand erstellt, ausgeführt und beendet. Ein dauerhafter Server-betrieb ist nicht erforderlich (Serverless)

down:

Bedeutung für die Cloud:

* Rechenkosten können nur genauer abgerechnet werden (Pay-per-Use auf Millisekunden - Basis)
* Rechenkosten entstehen wirklich nur bei Bedarf
* Leichtgewichtige Funktionen können schnell entwickelt und in den Betrieb überführt werden
* Management und Betrieb von Funktionen liegen in der Verantwortung des Cloud-Providers

down:

## IoT Cloud

* Smart Home, Connected Car sind aktuelle Themen die eine dedizierte Cloud Plattform verlangen
* Machine-to-Machine (M2M) Kommunikation auf Basis von unzuverlässigen Netzwerken benötigen Plattformen die gezielt auf diese Bedürfnisse zugeschnitten sind

down:

## IoT Cloud

* Message Queue Telemetry Transport (MQTT) ist ein Kommunikationsprotokoll welches für M2M entworfen wurde
* IoT Plattformen unterstützen MQTT und bieten Services ("Shadow Device" von AWS) an die für die Domäne IoT zugeschnitten sind

Beispiele: AWS IoT, Bosch IoT Cloud
