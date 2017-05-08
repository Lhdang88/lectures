## Was ist eigentlich ...

... Cloud Computing ?

<iframe width="560" height="315" src="https://www.youtube.com/embed/QJncFirhjPg" frameborder="0" allowfullscreen></iframe>

note: * Frage: Ist es eine Dienstleistung ? -> Ja, man mietet sich Rechenressourcen. Man lagert Assets (HW, Rechenzentren) aus und bucht die Services on Demand.
* Aus etwas physischem wird eine Dienstleistung
* Wie kann man diese Dienstleistung konsumieren / nutzen ? -> Über das Internet
* Beispiele:
  * Anwendungssoftware: Gmail, MS Office, Google Maps
  * Speicherplatz: Dropbox

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

down:

## Eigenschaften

Welche Eigenschaften lassen sich aus diesen Beschreibungen ableiten ?
<br>
<br>
1. (Self-)Provisioning (Selbstzuweisung) von Diensten
1. Zugriff über das Internet
1. Pay-per-Use

down:

#### Allgemein anerkannte Definition

<div style="text-align: left;">
_"... a model for enabling ubiquitous, convenient, <font color="DarkOrange" class="fragment" data-fragment-index="1">on-demand network access</font> to a <font color="DarkOrange" class="fragment" data-fragment-index="2">shared
pool</font> of configurable computing <font color="DarkOrange" class="fragment" data-fragment-index="3">resources</font> (e.g., networks, servers, storage, applications, and services) that
can be <font color="DarkOrange" class="fragment" data-fragment-index="4">rapidly provisioned</font> and released with minimal management effort or service provider interaction"_
<br>
<br>
<p style="color: LightSteelBlue;">
- National Institute of Standards and Technology (NIST)
</p>
<p style="font-size: 80%;">
[http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf](http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf)
</p>
</div>

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

down:

## weitere typische Eigenschaften

* Geografische Verteilung
* Multi-Mandantenfähigkeit
* Hohe Ausfallsicherheit
* Sicherheit: Verschlüssellung & Anonymisierung

![question](media/question.gif)<!-- .element: class="fragment" data-fragment-index="1" -->

down:

## Cloud Computing vs IT Outsourcing

Worin unterscheidet sich Cloud Computing von (klassischem) IT Outsourcing ?

Beispiel:

* Rechenzentrum wird übernommen
* Betrieb wird ausgelagert
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
