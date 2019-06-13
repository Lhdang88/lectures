### Computer Netzwerke

* Woraus besteht ein Computer Netzwerk ?
* <!-- .element: class="fragment" data-fragment-index="1" --> Firewall
* <!-- .element: class="fragment" data-fragment-index="2" --> Router, Switch
* <!-- .element: class="fragment" data-fragment-index="3" --> Loadbalancer
* <!-- .element: class="fragment" data-fragment-index="4" --> Network Interface Cards
* <!-- .element: class="fragment" data-fragment-index="5" --> etc.

Frage: wie sieht ein typisches Heimnetzwerk aus ?

down:

### Basics: Hub, Switch, Router

- Hub
- Switch
- Router

down:

### Basics: NAT

Wie kommunizieren Heim-Computer mit dem Internet ?

down:

### Network Address Translation (NAT)

<iframe width="560" height="315" src="https://www.youtube.com/embed/QBqPzHEDzvo" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

### Basics: IP Adresse (IPv4, IPv6)

- IPv4: 32-bit Adressraum
- private IPs vs public IPs
- private: 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12
- IPv6: 128-bit Adressraum

down:

### Virtuelle Netzwerke (am Beispiel Azure VNet)

* Was ist ein Virtuelles Netzwerk ?
* Was ist Netzwerkvirtualisierung

down:

### Netzwerkvirtualisierung

<img src="media/networkvirtualization.png" width="70%" height="70%"/>

down:

### Netzwerkvirtualisierung

* Abstrahierung von Netzwerk-Resourcen von Hardware-Komponenten
* Netzwerkkomponenten und Netzwerkfunktionen werden in Sofware repliziert
* die physikalischen Resourcen / Komponenten dienen zum Daten Transport
* die virtualisierten Komponenten steuern und definieren die Transportwege

down:

### NFV & SDN

* Techniken: Network Function Virtualization

* Entkopplung von Hardware-Resourcen von Funktionen
* Ziel: Optimierung/Effizienzsteigerung von Netzwerkfunktionen durch bessere Auslastung der Infrastruktur
* Network Functions: Firewall, Loadbalancing (L4-L7)

down:

### Network Function Virtualization
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/SIKxuFsx1l0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

### SDN

* Techniken: Software Defined Networking
* komplementär zu Network Function Virtualization
* dient dem Netzwerkmanagement: zentralisiert die Steuerung von Switches und Routern über APIs
* Einsatz: Cloud Computing zum steuern und bereitstellen von virtuellen Netzwerken
* Entkopplung von "Data-plane" und "Control-plane"

down:

### SDN

<iframe width="560" height="315" src="https://www.youtube.com/embed/lPL_oQT9tmc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

### SDN

<img src="media/SDN-Framework1.jpg" width="70%" height="70%"/>

down:

### Virtuelles Netzwerk

* entsteht durch die Anwendung von Netzwerkvirtualisierung(-techniken)
* es werden logische / nicht physikalische Netzwerke gebildet
* wired oder wireless

down:

### Motivation

* Welchen Nutzen bringt ein Virt. Netzwerk:

* Isolation: private network in der Cloud -> Security
* Performance: Direkte Kommunikation zwischen Netzwerk Komponenten (innerhalb des VNets) 
* Organisation: Backend Servers (DBs, Storage etc.) vs Internet Facing Servers (Web Apps)
* Kontrolle: security policies, DNS routing, FW-Regeln, Subnets

down:

### Frage vor der Pause

* Was ist das OSI Modell ?

<iframe width="560" height="315" src="https://www.youtube.com/embed/Hh3AYZf4bIk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

[OSI Modell](https://de.wikipedia.org/wiki/OSI-Modell)

down:

### Azure VNet

Features:

* Isolation & Segmentation
* Outbound/Internet Communication
* Network Security & Routing
* Azure Managed Services Integration
* On-Premises Communication (VPN)
* VNet Peering

[Azure VNet Overview](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

down:

### Azure VNet

<img src="media/azure-vnet.png" width="70%" height="70%"/>

down:

### Azure VNet Pricing

* VNet ist kostenfrei
* pro Subscription bis zu 50 VNets über alle Regionen
* Kostenpflichtig: Public IP Adressen, VPN Gateway, API Gateway, VMs, VNet Peering

[Azure VNet Pricing](https://azure.microsoft.com/en-us/pricing/details/virtual-network/)

down:

### Azure VNet

Network Security Groups (NSG)

* definiert Netzwerk Routing Regeln für Netzwerk Interfaces / Subnets (Firewall)
* Inbound Regeln und Outbound Regeln
* Regel besteht aus Name, Priorität, Source, Destination, Port, Action 

down:

### Azure Vnet

NSG

<img src="media/nsg.png" width="70%" height="70%"/>

down:

### VNet Subnets

* Was ist Subnetting ?
* Sementierung des Adressraums in Teilräume
* man verwendet häufig die Classless Inter-Domain Routing (CIDR-) Notation
* Nutzen: Organisation (Sicherheit), Performance, Vereinfachung von Routing

down:

### Azure VNet - Peering

* VNet Peering
* Wie können 2 VMs innerhalb 2 unterschiedlicher VNets miteinander kommunizieren ? (ohne über das Internet zu gehen)

down:

### Azure VNet - Peering

* VMs können direkt über ihre private IP miteinander kommunizieren
* Subnetze dürfen sich nicht überlappen (eineindeutigkeit der privaten IPs)
* Routing geschieht über die Azure Infrastruktur
* local VNet Peering: innerhalb einer Azure Region
* global Vnet Peering: zwischen Azure Regionen

[VNet Peering](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)

down:

### Azure VNet - Peering

* Vorteile: 
* Sicherheit - Traffic bleibt im Microsoft Backbone Network
* Performance - Traffic wird nicht indirekt über das Internet geroutet
* Datentransfer zwischen Subscriptions / Azure Services / Regionen werden ermöglicht

down:

### Azure IP Adressen

* public IPs - essentiell für Outbound Traffic
* private IPs - für traffic innerhalb eines VNets

down:

### Azure Public IP Adressen

* können folgenden Resourcen zugeteilt werden:
* VM Network Interfaces, Internet-Loadbalancers, VPN Gateways, Application Gateways (API Gateway)
* statische public IPs - fest zugeteilt, bspw. nützlich um eigene DNS Namen zu binden 
* dynamische public IP Adressen (ändern sich bei Restarts der zugeordneten Resource)
* IPv4 und IPv6 (nur bei Loadbalancer)

down:

### Cloud Networking - Loadbalancer

* Was ist ein Loadbalancer ?

<iframe width="560" height="315" src="https://www.youtube.com/embed/I86gp0Jcblw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

### Loadbalancer

* Typen: Hardware, Software Loadbalancer
* L4, L7 Loadbalancer
* Loadbalancer algorithmen: DNS round robin, gewichtetes round robin, least connection, affinity etc.

down:

### Azure Loadbalancer

* features:
* Loadbalancer algorithmen: source IP-hash basierte Verteilung, affinity basierte Verteilung

down:

### Zusammenfassung Azure VNets

<iframe width="560" height="315" src="https://www.youtube.com/embed/UYyRv-45OVM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
