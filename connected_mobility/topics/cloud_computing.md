## Was ist Cloud Computing?

<iframe width="560" height="315" src="https://www.youtube.com/embed/ae_DKNwK_ms?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

down:

## Cloud Computing ...

<div style="text-align: left;">_"beschreibt die <font color="DarkOrange" class="fragment" data-fragment-index="1">Bereitstellung von IT-Infrastruktur</font> wie beispielsweise Speicherplatz, Rechenleistung oder Anwendungssoftware als <font color="DarkOrange" class="fragment" data-fragment-index="2">Dienstleistung</font> über das <font color="DarkOrange" class="fragment" data-fragment-index="3">Internet</font>."_
<p style="color: LightSteelBlue;">
<br>
<br>
- Wikipedia
</p>
<p style="font-size: 80%;">
[https://de.wikipedia.org/wiki/Cloud_Computing](https://de.wikipedia.org/wiki/Cloud_Computing), 10.April.2017
</p>
</div>

down:

<div style="text-align: left;">
_"... Cloud Computing die <font color="DarkOrange" class="fragment" data-fragment-index="1">Bereitstellung von Computingdiensten</font> (Server, Speicher, Datenbanken, Netzwerkkomponenten, Software, Analyseoptionen und mehr) über das <font color="DarkOrange" class="fragment" data-fragment-index="2">Internet</font> („die Cloud“) ..."_

_"... Cloudanbieter ... stellen die Cloud Computing-Dienste üblicherweise <font color="DarkOrange" class="fragment" data-fragment-index="3">basierend auf der jeweiligen Nutzung in Rechnung</font>."_
<br>
<br>
<p style="color: LightSteelBlue;">
- Microsoft Azure,
</p>
<p style="font-size: 80%;">
[https://azure.microsoft.com/de-de/overview/what-is-cloud-computing/](https://azure.microsoft.com/de-de/overview/what-is-cloud-computing/), 10.April.2017
</p>
</div>

note:
* "stellen basierend auf der jeweiligen Nutzung in Rechnung" -> Pay-per-Use. -> Unterscheidung zu traditionellen Lizensmodellen / Pricing
* Frage: Welche Software Lizensmodelle kennt Ihr ?
* Traditionell Lizens (Dauerlizens / perpetual license): CD Kaufen Software nutzen so lange wie man will
* Subscription-based / Abos: monatlich, Jährlich, pro-User, Multi-User, Pro Instance/Core
* Pay-per-Use: - Datenvolumen, Transactions, Bandbreite, Storage Verbrauchsorientiert

down:

#### Allgemein anerkannte Definition

<div style="text-align: left;">
_"... a model for enabling ubiquitous, convenient, <font color="DarkOrange" class="fragment" data-fragment-index="1">on-demand network access</font> to a <font color="DarkOrange" class="fragment" data-fragment-index="2">shared
pool</font> of configurable computing <font color="DarkOrange" class="fragment" data-fragment-index="3">resources</font> (e.g., networks, servers, storage, applications, and services) that
can be <font color="DarkOrange" class="fragment" data-fragment-index="4">rapidly provisioned</font> and released with minimal management effort or service provider interaction"_
<br>
<br>
<p style="color: LightSteelBlue;">
- National Institute of Standards and Technology (NIST), 2009
</p>
<p style="font-size: 80%;">
[http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf](http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf)
</p>
</div>

note: Standardisierungsbehörde, allgemein wissenschaftlich als auch in der Industrie anerkannte Definition und Klassifizierung des Begriffs

down:

#### Essentielle Eigenschaften (NIST)

<table>
<tr>
  <td style="font-size: 50%; vertical-align: middle; text-align: left;">
    <font class="fragment" data-fragment-index="1">1. Kunden können sich zu jeder Zeit selbst Services zuordnen/bestellen ohne dass der Betreiber etwas tun muss</font>
    <br><br>
    <font class="fragment" data-fragment-index="3">3. Dienste können je nach Auslastung elastisch skalieren</font>
  </td>
  <td style="width: 50%;"><img src="media/NIST-Essential-Characteristics.svg" class="stretch"/></td>
  <td style="font-size: 50%; vertical-align: middle; text-align: left;">
    <font class="fragment" data-fragment-index="2">2. Dienste der Cloud werden über das Netzwerk (Internet/Intranet) bereitgestellt</font>
    <br><br>
    <font class="fragment" data-fragment-index="4">4. Resourcen des Cloud-Betreibers sind in einem Pool abstrahiert und können erweitert werden</font>
    <br><br>
    <font class="fragment" data-fragment-index="5">5. Dienste sind messbar, bspw. nach Resourcenverbrauch, Nutzungsdauer, Auslastung. Auswertungen sind für Cloud Betreiber und Kunden verfügbar</font>
  </td>
</tr>
</table>

note: * Was bedeutet self-provisioning
* was bedeutet Skalierung: der Dienst wächst und verkleinert sich mit der Last, dafür wird eine Automatisierungsmechanismus benötigt, welches 'Auto-Scaling' genannt wird, typische Eigenschaft der Cloud: 'Elastic Runtime'
* Resourcen pooling: Virtualisierung, je nach Bedarf werden physische Ressourcen hinzugefügt und in einem Pool zusammengeführt, bei Nutzung wird aus diesem bedient, die Platform kümmert sich um die Bereitstellung der Resourcen
* Messbarkeit: Metering durch Monitoring der Dienste, man kann durch einen Report die Nutzung zu jeder Zeit, Zusammenfassen lassen

down:

## weitere typische Eigenschaften

* Geografische Verteilung
* Multi-Mandantenfähigkeit
* Hohe Ausfallsicherheit
* Sicherheit: Sicherheitsstandards, Verschlüssellung & Anonymisierung

down:

## Cloud Computing vs IT Outsourcing

Worin unterscheidet sich Cloud Computing vom (klassischen) IT Outsourcing ?

Beispiel:

* Rechenzentrumsbetrieb wird ausgelagert
* Software wird per Spezifikation geschrieben und betrieben

note: * beides sind Dienstleistungen aus Sicht des Nutzers
* in beiden Fällen muss der Kunde sich nicht mehr um "Hardware, Software und Betrieb kümmern"
* der Kunde kann sich auf sein Business konzentrieren ...

* Cloud Computing (Systemdienstleister)
* bietet standardisierte Services für einen X-beliebigen Kunden (Multi-Tenant)
* Services sind On-Demand buchbar und skalierbar
* die Lokalisation der Kundendaten ist bei Cloud Computing intransparent
* die gemieteten Rechenressourcen sind dynamisch und verteilt

* Klassisches IT-Outsourcing: (Full-Service Dienstleister)
* bietet einen individuellen Service für einen bestimmten Kunden, Kundenwünsche können berücksichtigt werden
* Dienstleistungen können von Hosting, Entwicklung, Support etc. alles sein
* der Kunde teilt die gekauften Service-Leistungen nicht mit anderen Kunden (Single-Tenant)

down:

## Allgemeine Vorteile von Cloud Computing

* Kostenreduzierung
* Skalierung, 'scale-as-you-grow'
* höhere Verfügbarkeit, Ausfallsicherheit
* höhere Sicherheit
* schnellere Entwicklungsgeschwindigkeit

down:

## Nachteile von Cloud Computing

* Kontrollverlust: Compute Location, Storage Location
* Überprüfbarkeit: Sicherheitsstandards, Datenschutz Standards
* Potentielle Abhängigkeit: Vendor Lock-in, Tech Lock-in
* Sicherheit: erhöhte Gefahr durch Erreichbarkeit über das Internet

down:

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

note: * IaaS, PaaS, SaaS anhand eigener Skizze erklären
* traditionelle IT: welche Dinge muss man betreiben / managen um ein Software Produkt anbieten zu können

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

note: * Multi-Tenancy ist eine Querschnittsanforderung an das System
* Konzept könnte beinhalten wie Daten abgelegt werden, Tenant pro DB, Tenant pro Table, Tenant pro Row
* Tenant je nach RechnerCluster (Router, Datenschutz, Geo-Loadbalancing - Latenz)

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
