### Was ist High Availability (HA) ?

"... bezeichnet die Fähigkeit eines Systems, trotz Ausfalls einer seiner Komponenten mit einer hohen Wahrscheinlichkeit (oft 99,99 % oder besser) den Betrieb zu gewährleisten" - Wikipedia

down:

### Beispiele

- Internetdienste: Facebook, Google, E-Mails etc.
- Cloud Computing: VMs, Datenbanken, Loadbalancer, DNS Service etc.

down:

### SLAs, SLOs

- Service Level Agreements sind Vereinbarungen im Vertrag zwischen Cloud Provider und Nutzer, mit Zusicherungen (Bspw. Verfügbarkeit, Qualität) und Entschädigungen bei Nichteinhalten der Zusicherungen

- Service Level Objectives definieren messbare Ziele die als Zusicherungen in SLAs gemacht werden können

down:

### Beispiele: SLAs

- Azure DNS

"We guarantee that valid DNS requests will receive a response from at least one Azure DNS name server 100% of the time."

- Azure Databricks

"We guarantee that Azure Databricks will be available 99.95% of the time."

- [Azure SLAs](https://azure.microsoft.com/en-us/support/legal/sla/)

down:

### SLAs, SLOs, SLIs

<iframe width="560" height="315" src="https://www.youtube.com/embed/tEylFyxbDLE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- https://youtu.be/tEylFyxbDLE

down:

### Voraussetzung

Hochverfügbarkeit:

- redundante Komponenten / Funktionen
- ausfallsichere 'Connected Services'

down:

### High Availability

Die Nutzer erwarten von Systemen/Diensten/Funktionen die sie täglich / regelmäßig nutzen, dass sie immer erreichbar sind. Als hochverfügbar bezeichnet man Systeme die 99,99% und mehr "uptime" verfügen

down:

### High Availability

Was bedeutet "99,99%" (four nines)?

<img src="media/ha_table.png" width="70%" height="70%"/>

down:

### Wie berechnet man die Verfügbarkeit

Availablity = (uptime / uptime + downtime) * 100%

down:

### Wie berechnet man die Verfügbarkeit

oder über

- Availability = (MTBF / MTBF + MTTR) * 100%
- "Mean Time Between Failures"(MTBF)
<img src="media/mtbf.png" width="30%" height="30%"/>
- "Mean Time To Repair" (MTTR)

down:

### Verfügbarkeit: Komponenten in Serie / gekoppelt

Die Systemkomponente ist erreichbar wenn beide Teilkomponenten erreichbar sind.<br>

<img src="media/availability_calc1.png" width="30%" height="30%"/> <br>
Availability = Ax * Ay

down:

### Verfügbarkeit: Komponenten in Parallelbetrieb

Die Systemkomponente ist erreichbar wenn min. eines der Teilkomponenten erreichbar ist.<br>

<img src="media/availability_calc2.png" width="30%" height="30%"/><br>
Availability = ?

down:

### Wie erreicht man eine hohe Verfügbarkeit ?

Redundanz! 
- Hot Redundancy: Komponenten in Parallelbetrieb (Active/Active)
- Warm Redundancy: redundante Komponente im passiv Betrieb / Stand-By
- Cold Redundancy: redundante Komponente im "Lager", muss in Betrieb genommen werden

down:

### Wie erzeugt man Redundanz ?

Welche Komponenten können ausfallen ?
Welche Ebenen der Datenverarbeitung gibt es ?

down:

### Datacenter Redundanz

- Regions, Availability Zones
- redundante Strom-Generatoren, Internet Anbieter
- Kühlungssysteme
- Geo-Ip Routing, Traffic Routing um Daten zu verteilen

down:

## Beispiel: Azure High Availability

Realisierung: Regions & Zones & Sets

<iframe width="560" height="315" src="https://www.youtube.com/embed/PP02QxplC2E" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<font size="5">
<p>https://www.youtube.com/watch?v=PP02QxplC2E</p>
<p>https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability</p>
</font>

down:

### Netzwerk Redundanz

Redundante
- Router, Switches, Netzwerkkarten
- Loadbalancer, Firewalls
- Übertragungswege (Kabel - wie werden Kabelkanäle verlegt ? Wie werden Signale angenommen, Ethernet und Wifi) 

down:

### Server / Hardware Redundanz

Redundante:
- Festplatten: RAID
- CPU, Motherboards, RAM Sticks
- Stromversorgung

down:

### Software Redundanz

Redundante:
- Apps- / Service-Instanzen
- Datenbank-Instanzen, Caches

down:

### "Layer 8" Redundanz

- <!-- .element: class="fragment" data-fragment-index="1" -->Menschen ...
- <!-- .element: class="fragment" data-fragment-index="2" --> ... werden krank, gehen in den Urlaub

down:

### Wie designt man ein HA System ?

* Redundanz zieht sich durch alle Instanzen hinweg ...
* welche Probleme treten dabei auf ?
* mein System soll HA und konsistent sein ! (geht das ?)

down:

### Probleme: Verteilte Systeme

- Beispiel: Online Banking, Überweisung über Web-Site
- Anforderung: das System muss immer erreichbar sein, die Transaktionen sollen konsistent sein
- Verteilte Systeme bearbeiten Daten
- manche Daten sind "stateful", manche sind "flüchtig", manche Daten sollen persistiert werden

down:

### Probleme: Verteilte Systeme

- stateful: Login Session, Überweisungsdaten die über mehrere Seiten hinweg verwendet werden
- flüchtig (bspw. Daten die On-Demand errechnet werden): aktuelle Uhrzeit
- persistente Daten: Kontostand, Kunden-Daten

down:

### Probleme: Verteilte Systeme

- Um High Availability zu erreichen, betreibt man einen Cluster mit mehreren Instanzen einer Applikation
- Problem: Stateful-Daten müssen über alle Applikationsinstanzen hinweg verteilt (repliziert) werden
- zu persistierende Daten müssen in Datenbanken abgespeichert werden
- wie erreicht man eine hohe Verfügbarkeit bei Datenbanken ? 

down:

### Probleme: Verteilte Systeme

- Daten werden mehrfach (repliziert) und verteilt (sharding) abgespeichert
- wie erreicht man Konsistenz ? (alle Anfragen gegen die Datenbank liefern das gleiche Ergebnis zurück)
- Daten werden synchronisiert (abgespeichert)
- Was für ein Problem haben wir ?

down:

### CAP - Theorem für Verteilte Systeme

<img src="media/cap.png" width="70%" height="70%"/>

down:

### CAP - Theorem für Verteilte Systeme

<iframe width="560" height="315" src="https://www.youtube.com/embed/Jw1iFr4v58M" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

### CAP - Falsch: pick 2 out of 3

Netzwerk-Ausfälle sind die Realität! Entweder C oder A!

<img src="media/wrong_cap.png" width="70%" height="70%"/>

[https://codahale.com/you-cant-sacrifice-partition-tolerance/](https://codahale.com/you-cant-sacrifice-partition-tolerance/)

down:

### Fallbeispiel: MongoDB

- single Master, Master-Slave DB
- Master = reads/writes, genannt "primary node"
- Slave = read only, genannt "secondary nodes"
- consistency über availability

down:

### Fallbeispiel: Relationelle Datenbanken

- Bsp: MySQL, PostgreSQL etc.
- consistency über availability
- ACID (Atomicity, Consistency, Isolation, Durability) Tranksaktionen

down:

### Availability oder Consistency

- SQL vs NoSQL Datenbanken
- ACID vs BASE (Basically Available, Soft state, Eventual consistency)
- Eventual consistency = keine Consistency
- irgendwann werden alle Teilnehmer konsistent
- für HA und Skalierung

down:

### Frage

- Was ist Bitcoin/Facebook/Instagram/Amazon(Shopping Cart) für ein System ? CP oder AP ?
