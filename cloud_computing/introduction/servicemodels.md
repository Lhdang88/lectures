## Service Modelle

NIST Definition: 3 Service Modelle, hierarchisch gegliedert

<img src="media/Service-Model-Pyramid.svg" width="40%" height="40%"/>

down:

## noch mehr ... "as a Service"

... mittlerweile gibt es unzählige Formen von Cloud-Dienstleistungen die '... as-a-Service' genannt werden

* Container-as-a-Service (CaaS)
* Mobile Backend-as-a-Service (mBaaS)
* Security-as-a-Service (SecaaS)
...

* Sammelbegriff: Anything-as-a-Service (XaaS)

down:

#### noch mehr XaaS ! :)

* Cat-as-a-Service ([CataaS](http://cataas.com/))
* Ransomware-as-a-Service ([RaaS](https://www.heise.de/security/meldung/Ransomware-as-a-Service-Mit-Satan-den-eigenen-Erpressungstrojaner-bauen-3605326.html))
* Crime-as-a-Service ([Caas](https://www.heise.de/newsticker/meldung/Europol-warnt-vor-Crime-as-a-Service-aus-der-Cloud-3341301.html))
* Game-as-a-Service (Cloud Gaming, GaaS)

down:

## Infrastructure as a Service (IaaS)

* Ist die unterste Schicht des NIST-Service Modells
* Der Cloud-Provider kümmert sich um den Rechenzentrumsbetrieb, Hardware, Netzwerk und Speicher
* Rechenressourcen, Speicher, Netzwerkresourcen werden virtualisiert bereitgestellt
* Durch Virtualisierung kann der Kunde On Demand VM Instanzen bestellen

down:

Beispiel: Amazon Web Services

down:

## IaaS - Vorteile / Nachteile

<div style="text-align: left;">
+ freie Kontrolle über VMs, Betriebssystem, Software<br>
+ Kosten nach Nutzung<br>
+ kein Vendor Lock-in<br>
<br>
- VM Betrieb in eigener Verantwortung<br>
- langsame Entwicklungsgeschwindigkeit<br>
</div>

down:

## Platform as a Service (PaaS)

* mitlere Schicht im NIST Service-Modell
* Der Cloud-Provider stellt die Infrastruktur und eine Cloud-Plattform bereit.
* Die Plattform stellt vorgefertigte Laufzeitumgebungen bereit auf denen die Kundensoftware läuft.
* Es müssen keine VMs gepflegt und betrieben werden, stattdessen kann sich der Kunde um seine Software kümmern.

down:

## PaaS

<img src="media/PaaS-Simple.svg" width="50%" height="50%" style="background-color: white;" />

down:

## PaaS - Vorteile/Nachteile

<div style="text-align: left;">
+ upload von Source-Code in die Cloud, schnellere Entwicklungsgeschwindigkeit<br>
+ schnellere Time-to-Market<br>
+ geringerer Aufwand beim Kompetenzaufbau, fördert "DevOps"<br>
<br>
- Vendor lock-in möglich<br>
- ggfs. veraltete Laufzeitumgebungen (Abhängigkeit vom Patching des Plattform Betreibers)<br>
</div>

down:

## Software as a Service (SaaS)

* oberste Schicht im NIST Service Modell.
* Software wird als On-Demand Funktionalität zu jeder Zeit bereitgestellt.
* Der Cloud-Provider verantwortet den gesamten Stack: von Infrastruktur bis zur Applikation.
* Der Kunde ist lediglich nur noch für seine Daten verantwortlich.

down:

## SaaS

<img src="media/multi-tenancy.svg" width="50%" height="50%" style="background-color: white;" />

down:

#### Beispiele

* Office 365, Gmail, Google Docs
* Netflix, Spotify
* Salesforce.com

down:

## SaaS - Vorteile/Nachteile

<div style="text-align: left;">
+ Fokus auf das Kerngeschäft<br>
+ keine Verantwortung für Infrastruktur und Software<br>
+ Mobilität - die Software ist von Überall erreichbar<br>
<br>
- Vendor Lock-in wenn die Software exklusiv beim Cloud-Provider liegen<br>
- nur Standardsoftware erhältlich, nur eingeschränktes customizing<br>
</div>

down:

## Verantwortlichkeit

<img src="media/cloud-stack.png" width="70%" height="70%" />

down:

## Zusammenfassung

* Cloud Computing ist im Markt angekommen
* bringt große Vorteile für Unternehmen aller Größen
  * durch Skalierbarkeit, Kostenreduzierung, Verfügbarkeit, Sicherheit
* birgt allerdings auch Risiken
  * Kontrollverlust, Datenschutz, Vendor Lock-In

down:

## Zusammenfassung

* NIST 5-4-3 Regel:
 * 5 Eigenschaften, 4 Liefermodelle, 3 Service-Modelle
* es gibt verschiedene Hostingvarianten der Cloud
  * On-Premise, Off-Premise, self-managed, external-managed
* IaaS, PaaS, SaaS bedeuten für den Kunden eine Stufenweise Verschiebung der Verantwortung

down:

## Fragen ?

![questions](media/question2.gif)
