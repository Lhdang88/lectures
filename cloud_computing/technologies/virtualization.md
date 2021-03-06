## Virtualisierung

Frage: Welche Bedeutung hat Virtualisierung für Cloud Computing ?

<div style="white-space: nowrap">
<img src="media/the-thinker.jpg" width="40%" height="40%" />
<img src="media/thinking-monkey.png" width="40%" height="40%" />
</div>

down:

## Virtualisierung

essentiell u.a. für:
* Partitionierung von Ressourcen
* Skalierung / "Elastic Runtime"
* Sicherheit
* Multi-Tenancy
* Serverauslastung / Loadbalancing

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/FZR0rG3HKIk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<font size="4">https://youtu.be/FZR0rG3HKIk</font>

down:

## Virtualisierung

"... refers to the act of creating a virtual (rather than actual) version of something, including virtual computer hardware platforms, storage devices, and computer network resources."

- [Wikipedia](https://en.wikipedia.org/wiki/Virtualization), April.2017

note: beschreibt den Prozess aus etwas physischem oder nicht vorhandenem etwas virtuelles zu erzeugen
* beispiele für Virtualisierung: Netzwerkvirtualisierung: VPN
* Memory Virtualisierung: Virtueller Speicher (Pagetables, Prozesse können vom Betriebssystem virtuellen Speicher zugewiesen werden, der Speicher wird in Pagetables gespeichert, die Größe der Pagetables können n-bit groß sein, größer als der Hauptspeicher selbst, es können nur teile des speichers in RAM geladen werden)
* Storage-Virtualisierung: implementation in SAN-(Storage Area Network) um virtuelle Storage Pfade über einen pool aus physikalischen Festplatten zu abstrahieren, z.B. Cloud Storage

down:

#### Beispiel: Systemvirtualisierung

<img src="media/virtualization_win_on_osx.png" />
- https://www.virtualbox.org/

note: demo virtualbox
* demo virtual box configs

down:

#### Systemvirtualisierung

* versteht man eine Virtualisierungsschicht zwischen Hardware und OS
* Host-System: Basissystem auf dem die Virtualisierungsschicht läuft (Host-OS, Bare-Metal)
* Gast-System: Gast-Betriebssystem welches virtualisiert wird
* VM: Container in der das Gast-Betriebssystem läuft
* Was wird virtualisiert: CPU, Speicher, Storage, I/O, Netzwerk

down:

#### Systemvirtualisierung

* physische Resourcen werden partitioniert und abstrahiert bereitgestellt
* Hypervisor oder auch Virtual Machine Monitor (VMM) stellen Laufzeitumgebungen bereit
* Gast-Betriebssystem läuft in dieser Laufzeitumgebung mit virtualisierten Ressourcen (Speicher, Storage, Netzwerk, I/O)
* CPU-Operationen laufen direkt auf der unterliegenden Hardware (keine SW-Interpretation)
* I/O, Speicher- und Netzwerk-Operationen werden durch VMM umgeleitet

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

#### Systemvirtualisierung

* Kerneigenschaften:
  * Partitionierung der Resourcen - die verfügbaren Resourcen werden separiert den VMs bereitgestellt
  * Enkapsulierung - VM (-Zustand) wird durch ein Image-file abgebildet
  * Isolation - die VMs laufen unabhängig und voneinander getrennt (VMs können sich nicht beeinflussen)

down:

#### Systemvirtualisierung: Verwendung (Beispiele)

* Rechenzentrum
  * Steigerung der Auslastung durch mehrere VMs je phys. Server (z.B. 1 VM je App, Web- oder Application-Server oder Kunde)
  * Lastdistribution zwischen Servern: VMs werden durch Image-Files migriert
* Software Entwicklung
  * Testing: verschiedene Betriebssysteme, Konfigurationen, Software-Versionen werden durch Image-Files abgebildet
  * Distribution: Software Releases werden in ein Image-File verpackt und verteilt

down:

#### Emulation

[DOSBox](https://www.dosbox.com) - Emulator

<iframe width="560" height="315" src="https://www.youtube.com/embed/GZx-LJH5J_I" frameborder="0" allowfullscreen></iframe>

down:

#### Emulation

* Emulationssoftware, oder auch "Emulator", bildet ein System software-technisch ab
* ermöglicht Systeme zu simulieren welche nicht für die Host-Architektur ausgelegt sind
* im Gegensatz zur Virtualisierung läuft das zu emulierende System nicht direkt auf der CPU des Hosts ab
* Programm-Code welches im emulierten System läuft wird interpretiert

note: * Host-Architektur x86 CPU vs mobile ARM Architektur, Super Nintendo Hardware auf "65C816" CPU Architektur,
* die Emulationssoftware überbrückt Imkompatibilitäten durch emulierte Schnittstellen
* Beispiel Daemon Tools I/O DVD-/Blue-Ray Device Emulation

down:

#### Virtualisierung vs Emulation

* Virtualisierung ist performanter, mit weniger Overhead
* Virtualisierung abstrahiert Laufzeitumgebugen (CPU, Speicher, I/O)
* Emulation simuliert ein System über die Emulationssoftware
* Emulation ist flexibler aber deutlich langsamer als Virtualisierung (Emulation-Overhead)

down:

#### Emulation: Verwendung (Beispiele)

* Mobile Software Development (Android, IPhone - Emulatoren)
* Embedded Software Entwicklung (Steuergeräte in Autos, Haushaltsgeräte etc.)
* zum Abspielen alter Medien von nicht mehr unterstützter Hardware (SNES Emulator)
* Virtualisierung: zum simulieren von nicht vorhandener Hardware/inkompatibler Hardware
* Apple M1 Chip - Rosetta 2
<br>
<font size="4">https://www.computerworld.com/article/3597949/everything-you-need-to-know-about-rosetta-2-on-apple-silicon-macs.html</font>

down:

## Virtualisierung: VM vs Container

<iframe width="560" height="315" src='https://www.youtube.com/embed/cjXI-yxqGTI' allowfullscreen frameborder=0></iframe>
<br>
<font size="4">https://youtu.be/cjXI-yxqGTI</font>

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

#### Container: Vorteile

* effizient die Container laufen direkt auf dem Host-Betriebssystem bzw. teilen sich denselben Kernel
* das Gast-Betriebssystem muss nicht extra geladen werden
* Container-Images sind kleiner als VM-Images (lassen sich in Image-Repositories teilen)

note: * Frage: Wieviel RAM verbraucht ein modernes OS ? Mac OS, Win 10 ? 4GB, 6 GB, 8 GB ?

down:

#### Container: Nachteile

* Hosts können keine Fremdsysteme virtualisieren, wenn Sie nicht den gleichen Kernel haben
* Sicherheit: nicht so hoch bei VMs
  * Container teilen sich Kernel-Funktionen
  * keine vollständige Isolation: Fehler im Container können Einfluss auf geteilte Ressourcen haben
  * Ausbruch aus dem Container könnte direkt den Host kompromitieren

note: * Frage: Docker-Handson MacOS X, welcher Kernel benutzt Mac OSX ? Wie funktioniert Docker auf Mac OSX?
* (workaround: Boot2Docker ermöglicht trotzdem Docker-Container unter Win/Mac)
* Boot2Docker startet hierfür eine Mini-Linux VM (Docker Machine) in VirtualBox welche den Docker-Server beinhaltet und mit dem Docker-Client auf dem Host kommuniziert / steuerbar ist (REST API)

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/0qotVMX-J5s" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<font size="4">https://youtu.be/0qotVMX-J5s</font>

down:

#### Bedeutung von VMs für Cloud Computing

* bieten Sicherheit durch Isolierung
* Multi-Tenancy: Kunden teilen sich denselben Server, aber arbeiten getrennt voneinander (durch Isolation)
* ermöglicht dass VM-Instanzen zwischen Servern "wandern" (durch Enkapsulierung in VM-Images)
* flexiblere und bessere Auslastung von physischen Servern
* Grundbaustein für IaaS

down:

#### Bedeutung von Container für Cloud Computing

* effizienter als VMs
  * schnellere Skalierbarkeit durch schnelleres Boot-up
  * Container können effizienter zwischen VM-Instanzen "wandern" (leichtgewichtigere Container-Images)
  * eignen sich besser um Software Komponenten zu kapseln (Apps, DB, Software-LB, Web-Server etc.)
  * essentielle Grundlage für PaaS, CaaS und auch Serverless (OpenWhisk)

down:

#### VM-Einsatz bei IaaS (AWS-Elastic Compute Cloud)

* Amazon Machine Image (AMI) bilden konfigurierten Stand einer VM-Instanz ab
* beliebig viele VM-Instanzen können durch ein AMI gestartet werden
* VM-Instanzen sind in EC2 volatil, d.h. der Lebenszyklus einer VM wird durch EC2 bestimmt
* Scale-Up: zusätzliche VM-Instanzen gestartet
* Scale-Down: VM-Instanzen werden terminiert

[https://aws.amazon.com/de/ec2/](https://aws.amazon.com/de/ec2/)

down:

#### AWS EC2 - Instance Lifecycle

<img src="media/ec2-instance-lifecycle.png" width="70%" height="70%" />
<font size="5">
- http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-lifecycle.html
</font>

down:

#### Beispiele für Container PaaS

- AWS Elastic Kubernetes Service (EKS), Azure Kubernetes Service (AKS), Google Kubernetes Engine (GKE)
- AWS Elastic Container Service (ECS), Azure App Service, Google App Engine
- AWS Lambda, Azure Functions, Google Cloud Run
- CloudFoundry
