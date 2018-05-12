## Technische Entwicklung & Trends in Cloud Computing

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
* AWS 2006, IaaS, CapEx to OpEx (Investitionsausgaben zu Betriebsausgaben), AMI (Amazon Machine Image = VM), VMs on Click, Automatisierung von VMs boot-up, elastic runtime , closed source
* Heroku 2009, PaaS, neue Software Entwicklungskonzepte: Microservices, 12-Factor Apps, faster time to market, Buildpacks, closed source
* OpenStack 2010, open source IaaS, Zusammenschluss vieler Unternehmen um Open Source IaaS zu entw., Nasa, Rackspace
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

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-pulls-stats.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey2.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey3.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey4.png)
</div>

down:

## Wie funktioniert Docker ?

Betriebssystem-level Virtualisierung

* Systemvirtualisierung vs Betriebssystem-Virtualisierung

down:

#### Systemvirtualisierung

<img src="media/intel-virtualization.png" width="70%" height="70%"/>

<font size="4">
[https://software.intel.com/en-us/articles/the-advantages-of-using-virtualization-technology-in-the-enterprise](https://software.intel.com/en-us/articles/the-advantages-of-using-virtualization-technology-in-the-enterprise)
</font>

down:

#### Systemvirtualisierung

<img src="media/virtualization-example.png" width="60%" height="60%"/>

note: * das Gast-Betriebssystem ist mit der Hardware-Architektur des Hosts Kompatibel (CPU: gleicher Befehlssatz, bei nicht vorhandender HW/Imkompatibilität -> Emulation)
* es gibt Hardware Hypervisor (CPU), oder Software Hypervisor (laufen im OS)
* wie kann ein Programm im Gast-OS direkt auf der Host-CPU laufen ? Programme werden zu Maschinen-Code (Befehlssatz x86) kompiliert
* Beispiel: Win, Linux Unterstützung für x86, aber auch Android x86

down:

#### Betriebssystem-Virtualisierung

* Idee: keine vollständige Virtualisierung des Gast-Systems, d.h. VM-Betriebssystem soll nicht komplett geladen werden, sondern stattdessen direkt auf dem Host-Betriebssystem laufen
* der OS-Kernel stellt Funktionen bereit, damit Prozesse isoliert auf Speicher, Storage, I/O-, Netzwerk- und andere OS-Funktionalitäten zugreifen können
* bei Linux (Docker) wird die Isolierung über "cgroup" (Partitionierung von CPU, Speicher, File-System, Netzwerk) und "namespaces" realisiert
* partitionierte Umgebung wird "Container" genannt

note: * Frage: Was ist ein OS-"Kernel", welche Kernel kennt ihr ?
* NT-Kernel, Linux-Kernel, Darwin-Kernel etc.
* VL-Betriebssysteme: Aufgaben eines Betriebssystem, CPU Management, Speicher-(Page-Tables), File System-Management, I/O, Treiber-Management
* Was ist virtueller Speicher ? Beispiel Speicher-Virtualisierung. Page Tables
* Betriebssystem-Virtualisierung, engl. OS-Level Virtualization, weil das Betriebssystem die Virtualisierungsumgebung bereitstellt

down:

#### Betriebssystem-Virtualisierung vs Systemvirtualisierung

![container-vs-vm](media/container-vs-vms.jpg)

note: * es wird kein Hypervisor / Virtual Machine Monitor benötigt
* die Container laufen direkt auf dem Host-Betriebssystem bzw. teilen sich denselben Kernel
* Container-Images sind viel kleiner als VM-Images, da das Betriebssystem nicht gespeichert werden muss
* weniger Overhead, da direkt Kernel-Funktionen genutzt werden
* Overhead: VMs nutzen Kernel-Funktionen des Gast-Betriebssystem, diese Funktionalitäten werden durch den Hypervisor an die CPU, Speicher, IO umgeleitet

down:

#### Frage: Wie nennt man folgende Art von Software?

![emulation](media/emulation.jpg)

down:

#### Container Orchestrierung

![containers](media/containers.gif)

down:

## Container Orchestrierung

* Framework verantwortlich für Container Life-cycle, Scaling, Networking, Loadbalancing, Virtual Storage
* Container kommunizieren über ein privates Netzwerk miteinander
* Kommunikation nach extern über externes Netzwerk
* "Bring-your-own-Container"-Prinzip: die Plattform startet beliebige Container-Images
* Container Images werden in Image-Repositories hochgeladen (public/private)

down:

Bedeutung für Cloud Computing

* Basis für Container-as-a-Service (CaaS)
  * flexibler als PaaS, einfacher als IaaS
  * CaaS als Alternative zur PaaS und IaaS
  * DevOps-Orientiert
* Kein Vendor Lock-in
  * Kubernetes ist open-source, integrierbar in private / public cloud

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

* Rechenkosten können genauer abgerechnet werden (Pay-per-Use auf Millisekunden - Basis)
* Rechenkosten entstehen wirklich nur bei Bedarf
* Leichtgewichtige Funktionen können schnell entwickelt und in den Betrieb überführt werden
* Management und Betrieb von Funktionen liegen in der Verantwortung des Cloud-Providers

Beispiele:

AWS Lambda, Apache OpenWhisk, Google Cloud Functions

