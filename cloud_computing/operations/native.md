### Cloud Native ...

Was ist Cloud Native

"Cloud native computing is an approach in software development that utilizes cloud computing to 'build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds'"

<font size="4">https://en.wikipedia.org/wiki/Cloud_native_computing</font>

down:

### Cloud Native

Es ist ein Software Design Prinzip um (, in einer Cloud Umgebung):

- die Vorteile von Cloud Computing auszuschöpfen (Skallierbarket, Robustheit, Effizienz)
- Kommunikationsstandards wieder zu verwenden
- Wartbarkeit und den Betrieb erhöhen
- Software Design zu vereinfachen (Entkopplung von spezifischer On-Prem. Hardware/Software Restriktionen)

down:

Cloud Native Computing Foundation (CNCF)

- Linux Foundation Projekt / Konsortium, bestehend aus Personen und Firmen aus der Software Industrie
- Ziel: Entwicklung von Software in der Cloud zu standardisieren/zu vereinfachen
- fördert Best-Practices (Microservice, DevOps), Frameworks und Technologien
<br>
<font size="4">https://www.cncf.io</font>

down:

Cloud Native Landscape 2021

<img src="media/cloudnativelandscape.png" width="75%" height="65%"/>
<br>
<font size="4">https://landscape.cncf.io/</font>

down:

### Cloud Native ...

Cloud Native Apps

- Container
- Microservices
- DevOps, CI/CD
- Standardized APIs (RESTful, gRPC, Open API)
- 12-Factor Apps (https://12factor.net/de/)

down:

### Cloud Native ...

Cloud Native Apps

<iframe width="560" height="315" src="https://www.youtube.com/embed/9Ik96SBaIvs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<p>
<font size="4">https://youtu.be/9Ik96SBaIvs</font>

down:

### Cloud Native ...

Architecture: Microservices

* Architektur: Dekomposition von Monolithen in eigenständige Microservices
* Offene Schnittstellen, keine proprietäre Protokolle, meistens RESTful (Http) o. Message Brokers/Queues
* best-suit für Microservice: Programmiersprache, Framework
* Klar voneinander abgegrenzte Verantwortungsbereiche (Business Logik)

down:

### Vorteile

* unabhängige Skalierbarkeit von Microservices
* versteckte Abhängigkeiten werden über die API erkennbar
* Sprachenunabhängig, Teams können nach ihren Wünschen den Technologiestack auswählen
* unabhängige Entwicklungszyklen, Parallelisierung der Entwicklung

down:

### Nachteile

* Performance Overhead durch Netzwerk-Kommunikation
* Erhöhte Komplexität von Tests: Unit/Komponenten-Tests werden Integrationstests
* Erhöhte Komplexität von Monitoring: zentralisiertes Monitoring, Splunk, AppDynamics etc.
* Deployment Prozess muss ggfs. zwischen Teams abgestimmt werden (API Breaking Changes)

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/CKL3fV5UR8w" frameborder="0" allowfullscreen></iframe>
<p>
<font size="4">https://youtu.be/CKL3fV5UR8w</font>

down:

### DevOps

<img src="media/devops.jpg" width="75%" height="65%"/>
<br>
<font size="4">https://www.information-age.com/automating-six-cs-devops-123488662/</font>

down:

### DevOps

- Kombination aus Software Development & Operations
- Vereint Tätigkeiten & Prozesse in beiden Gebieten
- überbrückt Abhängigkeit und Fehleranfälligkeit zwischen Dev & Ops
- erhöht die Effizienz zwischen den beiden Prozessen
- geeignet für Cloud Computing (schnelligkeit, agilität, skallierbarkeit)

down:

### Cloud Native ...

Datenbanken (DBaaS)

- Cloud Native design
- managed service (e.g. updates, security, backup/recovery)
- skallierbar, resilient

down:

<img src="media/cloudnativedb.png" width="75%" height="65%"/>
<br>
<font size="4">https://en.wikipedia.org/wiki/Cloud_database</font>

down:

<img src="media/cloudnativetechnologien.png" width="75%" height="65%"/>
<br>
<font size="4">https://de.cloudflight.io/presse/top-10-cloud-native-technologien-fuer-den-unternehmenseinsatz-35416/</font>