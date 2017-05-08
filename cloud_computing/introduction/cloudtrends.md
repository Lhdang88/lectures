## Container

Was sind Container?

* Virtuelle Laufzeitumgebung (Container) die auf einem Betriebssystem (Host) laufen
<br>
<br>
Typische Features:

* Isolierte Laufzeitumgebung (Prozesse, Memory, Netzwerk, Storage)
* Virtualisierte Netzwerkumgebung
* Limitierbarkeit von CPU, Memory-Auslastung

down:

Container vs Virtuelle Maschine (Betriebssystem Virtualisierung vs Systemvirtualisierung)

![container-vs-vm](media/container-vs-vms.jpg)<!-- .element: class="fragment" data-fragment-index="1" -->

note: Frage - was sind die Vorteile von Virtuellen Maschinen ggü. Container ?

down:

<div class="stretch">
  <img src="media/docker-container-example.png"/>
</div>

down:

Vorteile:<!-- .element: style="text-align: left;" -->
 * effizient (geringerer Speicherverbrauch, gemeinsame Nutzung von Host-Bibliotheken (Linux Kernel)
 * Prozess-Isolation
 * Schnelles Laden der Laufzeitumgebung

Nachteile:<!-- .element: style="text-align: left;" -->
 * Hosts können keine Fremdsysteme virtualisieren (workaround: Boot2Docker ermöglicht trotzdem Docker-Container unter Win/Mac)
 * Sicherheit (todo: link)

note: Boot2Docker startet hierfür eine Mini-Linux VM (Docker Machine) in VirtualBox welche den Docker-Server beinhaltet und mit dem Docker-Client auf dem Host kommuniziert / steuerbar ist (REST API)

down:

Bedeutung für Cloud Computing

* Bietet Isolierte Laufzeitumgebungen für Anwendungen (Apps, Datenbanken, Message Queues etc.)
* Einsatz als konsequente Folge der effizienteren Auslastung der Resourcen im Vgl. zu VMs (Bspw. Cloud Foundry, Kubernetes)
* Schnellere Verfügbarkeit bringt Vorteile für Application-Level Skalierung (PaaS) bzw. auch für Lambda-Funktionen (Serverless)

down:

Beispiel: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-pulls-stats.png)
</div>

down:

## Container Orchestrierung

* Frameworks die es ermöglichen verschiedene Container in einem Netzwerk zu verbinden
* Container können im (geschlossenen) virtuellen Netzwerk miteinander Kommunizieren (App-Container mit DB-Container)
* Container können von einem Container Host transparent zu einem anderen wandern
* Horizontale Skalierung von Container - das Framework überwacht die Last einzelner Container und skaliert auf Wunsch automatisch

down:

Bedeutung für Cloud Computing

* Container Frameworks sind ein mächtiges Werkzeug um effizient Systeme auf Applikations/Service-Ebene aufzusetzen und zu betreiben.
* Flexibler als die Standard Werkzeuge von Cloud-Anbietern.
* Kein Vendor Lock-in, man kann mit dem Framework auf eine andere Platform migrieren
* CaaS als Alternative zur PaaS.

down:

Beispiel:

<div class="stretch">
<table>
<tr>
  <td width="40%" height="40%">
    ![Kubernetes](media/kubernetes.png)
    <br>
    [Kubernetes](https://kubernetes.io/)</td>
  <td width="40%" height="40%">
    ![Docker-Swarm](media/docker-swarm.png)
    <br>
    [Docker Swarm](https://docs.docker.com/engine/swarm/)</td>
</tr>
</table>
</div>

down:

## Serverless

![Serverless-Lambda](media/Lambda_HowItWorks.png)

down:

* Serverless != Ohne Server
* kurzlebige Funktionen (stateless)
* In Serverless-Funktionen können On-Demand Rechenoperationen implementiert werden, die nicht ständig laufen müssen
* Lambda-Funktionen werden in der CLoud On-Demand erstellt, ausgeführt und beendet
* Die Kosten werden im Pay-per-Use Prinzip in Millisekunden abgerechnet

down:

Bedeutung für Cloud Computing

* Rechenkosten können nur genauer abgerechnet werden (Pay-per-Use auf Millisekunden - Basis)
* Rechenkosten entstehen wirklich nur bei Bedarf
* Leichtgewichtige Funktionen können schnell entwickelt und in den Betrieb überführt werden
* Management und Betrieb von Funktionen liegen in der Verantwortung des Cloud-Providers

Beispiele:

AWS Lambda, Apache OpenWhisk, Google Cloud Functions

down:

## IoT Cloud

* Smart Home, Connected Car sind aktuelle Themen die eine dedizierte Cloud Plattform verlangen
* Machine-to-Machine (M2M) Kommunikation auf Basis von unzuverlässigen Netzwerken benötigen Plattformen die gezielt auf diese Bedürfnisse zugeschnitten sind

down:

## IoT Cloud

* Message Queue Telemetry Transport (MQTT) ist ein Kommunikationsprotokoll welches für M2M entworfen wurde
* IoT Plattformen unterstützen MQTT und bieten Services ("Shadow Device" von AWS) an die für die Domäne IoT zugeschnitten sind

Beispiele: AWS IoT, Bosch IoT Cloud
