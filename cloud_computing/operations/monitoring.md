### Cloud Monitoring

Was ist Monitoring ?

<img src="media/devops.jpg" width="75%" height="65%"/>
<br>
<font size="4">https://www.information-age.com/automating-six-cs-devops-123488662/</font>

down:

Ziel

- Software sichtbar machen
- Resourcen(verbrauch) messen
- Benutzer Eingaben darstellen
- Fehler melden
- usw.

down:

### Cloud Monitoring vs On-Prem Monitoring

- Microservice Architekturen vs Monolithen
- Verteilte Infrastruktur vs 'Alles auf einem Server'
- Zentrale Monitoring Plattform vs viele lose Monitoring Tools

down:

### Anforderungen Cloud Monitoring

- Alles auf einem Blick
- Events aus verteilten Systemen miteinander kombinieren (bspw. zeitlich ordnen)
- verschiedene Technologie-stacks integrieren: DBs, VMs & Container, Programmiersprachen-Runtimes (Java, .Net, Javascript)
- Visuell aufbereiten: Diagramme, Dashboards etc.
- Alerting: Benachrichtigungen per E-mail, Slack, SMS, Webhooks etc.

down:

### Produkte

Cloud Provider

- AWS Cloudwatch
- Azure Monitoring
- Google Cloud Monitoring

down:

Monitoring SaaS

- Datadog
- New Relic
- AppDynamics
- Splunk

down:

OpenSource

- Elastic Search (+Logstash,+Kibana) - ELK
- Grafana

down:

Azure Monitoring

<img src="media/azuredashboard.png" width="75%" height="65%"/>

down:

Datadog

<img src="media/datadogdashboard.png" width="75%" height="65%"/>

down:

Grafana

<img src="media/grafanadashboard.png" width="75%" height="65%"/>

down:

Dynatrace

<img src="media/dynatracedashboard.png" width="75%" height="65%"/>

down:

Elasticsearch (ELK)

<img src="media/elkdashboard.png" width="75%" height="65%"/>

down:

Welche Arten von Monitoring gibt es ? (Beispiele)

- Anwendungsmonitoring (Application Performance Monitoring)
- Infrastruktur Monitoring
- Security Monitoring

down:

### Application Performance Monitoring

<iframe width="560" height="315" src="https://www.youtube.com/embed/27lDUFBUTko" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>
<font size="4">https://youtu.be/27lDUFBUTko</font>

down:

### Application Performance Monitoring

- Wieviele Requests ?
- Was ist die avg. Request-Latency ? Latency von Request 'XYZ' ?
- Wo gibt es Bottlenecks (Request Tracing)? Im Code, DB-Query, Netzwerk, I/O ?
- Gibt es Errors ?

down:

### Application Performance Monitoring

- Integration bei Java, .Net, Javascript durch Agents (JVM, NodeJS-Module)
- Misst Dauer für Funktionsaufrufe, DB-Queries
- CPU & Memory Auslastung per Runtime
- Co-Relation von events durch Trace-Ids oder Zeitstempel

down:

### Infrastruktur Monitoring

<iframe width="560" height="315" src="https://www.youtube.com/embed/e2E7RroTAck" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>
<font size="4">https://youtu.be/e2E7RroTAck</font>

down:

### Infrastruktur Monitoring

- Wie ist der Resourcen verbrauch ?
- Wieviele VMs/Container laufen ? Wie ist die aktuelle Skallierung ?
- Netzwerk Traffic ? Festplatten-Verbrauch ?

down:

### Infrastruktur Monitoring

- bei Kubernetes per Kubernetes Monitoring Service
- VMs in Clouds per Abfrage über OS / Runtime
- Skallierung: per Anfrage an Service-API (@Kubernetes wieviele Pod-Instanzen laufen ?)

down:

Wie wird Cloud Monitoring Umgesetzt ?

<iframe width="560" height="315" src="https://www.youtube.com/embed/gyDp-Cl_MdA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<font size="4">https://youtu.be/gyDp-Cl_MdA</font>

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/S36jEgS8EJc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<font size="4">https://youtu.be/S36jEgS8EJc</font>
<br>
<font size="4">Solarwinds-Hack: https://www.golem.de/news/cyberangriff-auf-die-usa-beim-solarwinds-hack-geht-es-um-mehr-als-spionage-2101-153121.html</font>

down:

### Welche Formen von Monitoring Daten gibt es ?

- Logs
- Metriken
- Traces

down:

### Logs

- sind spezifische Informationen über einen Zustand zu einem Zeitpunkt
- für Debugging und konkrete Fehleruntersuchung
- können bei vielen Requests stark wachsen, nicht skallierbar (kostenintensiv)
- Bsp: Error-Logs, Access Logs (User XY hat sich um 20:11:35 eingeloggt)
<br>
<img src="media/logs.png" width="55%" height="45%"/>

down:

### Metriken

- sind Kennzahlen über einen Zustand aggregiert über einen Zeitraum
- helfen bei der Fehleruntersuchung
- können aber keine Aussage über ein bestimmtes Problem zu einem spezifischen Zeitpunkt geben
- skallierbar, da Informationen als Kennzahl aggregiert werden (praktisch keine Kosten)
- Bspw: Request pro minute/stunde/tag, avg./min./max. Verarbeitungsdauer
<br>
<img src="media/metrics.png" width="75%" height="65%"/>

down:

### Weiterführende Informationen: Metriken mit Prometheus

<iframe width="560" height="315" src="https://www.youtube.com/embed/XToKHYXSUyc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>
<font size="4">https://youtu.be/XToKHYXSUyc</font>

down:

### Traces

- sind verkettete Informationen über eine Transaktion im System
- für Debugging und konkrete Fehleruntersuchung in einem Verteilten System
- Bsp: 
  - Trace t1 = Request X erhalten 20:11:35 in Microservice A 
  - Datenbank Abfrage um 20:11:36
  - Datenbank Abfrage fertig um 20:11:38
  - Weiterleitung an Microservice B um 20:11:40
  - Dauer Trace t1 gesamt = 5s, DB-Query=2s

down:

### Distributed Tracing

<iframe width="560" height="315" src="https://www.youtube.com/embed/v5xnBcliJbE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>
<font size="4">https://youtu.be/v5xnBcliJbE</font>

down:

### Alerting

- Auf Basis von Logs, Metriken, Traces
- Bsp: Wenn: Request-per-minute > 1000, Dann: Skalliere auf Cluster Node=2
- Informiere DevOps-Nachrichten Kanal in MS Teams/Slack

down:

### Setup in Google Cloud Platform

<iframe width="560" height="315" src="https://www.youtube.com/embed/IHbwrBixLAQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>
<font size="4">https://youtu.be/IHbwrBixLAQ</font>
