### Was ist High Availability (HA) ?

"... bezeichnet die Fähigkeit eines Systems, trotz Ausfalls einer seiner Komponenten mit einer hohen Wahrscheinlichkeit (oft 99,99 % oder besser) den Betrieb zu gewährleisten" - Wikipedia

down:

### Beispiele

- Internetdienste: Facebook, Google, E-Mails etc.
- Cloud Computing: VMs, Datenbanken, Loadbalancer, DNS Service etc.

down:

### Beispiel aus der Automobilindustrie:

- Automatisiertes Fahren: Level 0 - Level 5

<img src="media/AD_levels.jpg" width="70%" height="70%"/>

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

down:

### Netzwerk Redundanz

Redundante
- Router, Switches, Netzwerkkarten
- Loadbalancer, Firewalls
- Übertragungswege (Kabel - wie werden Kabelkanäle verlegt ? Wie werden Signale angenommen, Ethernet und Wifi) 

down:

### Server Redundanz

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

- Um High Availability zu erreichen, betreibt man einen Cluster bzw. mehrere Instanzen einer Applikation
- Stateful-Daten müssen über alle Applikationsinstanzen hinweg verteilt (repliziert) werden
- zu persistierende Daten müssen in Datenbanken abgespeichert werden
- Auslagerung in einer Datenbank oder Cache oder Netzwerk Storage (Festplatte)

down:

### Probleme: Verteilte Systeme

- wie erreicht man eine hohe Verfügbarkeit bei Datenbanken ? 
- Daten werden mehrfach (repliziert) und verteilt (sharding) abgespeichert
- wie erreicht man Konsistenz ? (alle Anfragen gegen die Datenbank erhalten das gleiche Ergebnis)
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

### Abschlussfrage

- Was ist Bitcoin für ein System ? CP oder AP ?

down:

## Fragen zur Klausur ?