### Digitalisierung ...

* Traditionelle Unternehmen verkaufen physische Produkte und Dienstleistungen
* Arbeitsprozesse basieren auf analogen Medien, keine Vernetzung der Informationsquellen
* Digitale Vertriebskanäle nicht vorhanden, keine schnelle globale Verbreitung möglich

down:

* Traditionelle analoge Prozesse und auf physischen Dingen basierende Geschäftsmodelle werden digitalisiert
* durch Möglichkeiten der Digitalisierung entstehen Disruptionen:
  * Netflix, Uber, Amazon, Spotify usw.
* Folgen: aus traditionellen Unternehmen ("Hardware Hersteller") werden IT-Service Unternehmen
* Cloud Computing ist ein Enabler für digitale Disruption, da diese die Skalierung der IT mit dem Geschäftsmodell ermöglicht

note: * Netflix revolutionierte den Video Verleihmarkt
* Uber macht traditionelle Taxi Unternehmen überflüssig
* Amazon: König von E-Shopping
* Spotify: Musik-markt verkauft keine CDs mehr

down:

### Die Vorteile von Cloud Computing (Wiederholung)

 * Reduzierung von Total Cost of Ownership (TCO)
 * Elastische Skalierung durch Automatisierung und Virtualisierung
 * Agilität durch On-Demand Bereitstellung Infrastruktur und Services
 * Kostenreduktion und Flexibilität durch dynamisches Kostenmodell (Pay-per-Use)
 * Schnellere Time to Market, z.B. durch On-Demand Dienste, höhere Entwicklungsgeschwindigkeit
 * Geografische Abdeckung des Cloud-Providers

down:

### Technische Entwicklung & Trends in Cloud Computing

<span style="white-space: nowrap">
<img src="media/cncf1.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="1" /><img src="media/cncf2.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="2" /><img src="media/cncf3.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="3" /><img src="media/cncf4.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="4" /><img src="media/cncf5.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="5" /><img src="media/cncf6.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="6" /><img src="media/cncf7.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="7" /><img src="media/cncf8.png" width="130px" height="230px" style="border: 0px solid #eee;
    box-shadow: 0 0 0px rgba(0, 0, 0, 0.15);" class="fragment" data-fragment-index="8" />
</span>

note: * 2000's new Website? buy bare metal, sun's market, Building Block ist physischer Server - Metall
* VMWare, Server Virtualisierung, effizienter als Bare-Metal Server (Auslastung ~10%),Building Block ist VM
* AWS 2006, IaaS, CapEx to OpEx (Investitionsausgaben zu Betriebsausgaben), AMI (Amazon Machine Image = VM), VMs on Click, Automatisierung von VMs boot-up, elastic runtime , closed source, (Vendor-Lockin)
* Heroku 2009, PaaS, neue Software Entwicklungskonzepte: Microservices, 12-Factor Apps, faster time to market, Buildpacks, closed source (Vendor-Lockin)
* OpenStack 2010, open source IaaS, Zusammenschluss vieler Unternehmen um Open Source IaaS zu entw., Nasa, Rackspace, Open-Source gegen Vendor-Lockin
* Cloud Foundry, open source PaaS, Buildpacks, vergleichbar mit Heroku, Container
* Docker, real Container Magic, Building Block ist Container, DevOps Parität, Dev=Ops, gleiche Umgebung durch Docker
* Kubernetes, Orchestrierung auf Basis von Docker, von Google, Management von Zehn-/Hunderttausend Containern gleichzeitig, neues Cloud Modell: CaaS
* Isolation Level von Server, VM zu Container
* Boot-up Time von Bare-Metal Setup (weeks), VM(Minutes), Container (seconds)

down:

<img src="media/cncf-cloud-customized.png" width="70%" height="70%"/>
<br>
* verändert, Original von [CNCF Keynote - A Brief History Of The Cloud](http://events.linuxfoundation.org/sites/events/files/slides/CNCF%20Keynote%20Preso.pdf)

down:

#### Cloud Native Computing Foundation

* 2015 gegründet, Teil der Linux-Foundation
* Open Source Konsortium um Open Source Cloud Computing insbesondere Container-Technologien zu promoten und zu steuern
* organisiert jährlich Konferenzen in USA, Europa und Asien
* identifiziert Technologien die für Cloud Computing relevant sind

down:

#### CNCF Landscape 2017

<img src="media/cncf-landscape.jpg" width="80%" height="80%"/>
