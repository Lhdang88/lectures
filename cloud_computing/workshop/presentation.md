## Cloud Computing ...

<table>
<tr>
  <td style="width: 50%;"><img src="media/cloud-char-confused.svg" class="stretch"/></td>
  <td style="font-size: 80%; vertical-align: middle; text-align: left;">
    ... ein Buzzwort ?
    <br><br>
    ... ein Hype ?
    <br><br>
    ... "ist doch nicht neu ! Gab's früher auch schon ..."
  </td>
</tr>
</table>

down:

## Was ist eigentlich ...

... Cloud Computing ?

<iframe width="560" height="315" src="https://www.youtube.com/embed/QJncFirhjPg" frameborder="0" allowfullscreen></iframe>

down:

#### Bespiele bekannter Cloud-Dienste, Stand 2017

<table>
<tr>
  <td style:"width: 25%;"><img src="media/AWS-Logo.png" style="width: 250px; height: 100px;"/></td>
  <td style:"width: 25%;"><img src="media/azure-logo.png" style="width: 150px; height: 100px;"/></td>
  <td style:"width: 25%;"><img src="media/GCP-Logo.png" style="width: 250px; height: 100px;"/></td>
</tr>
<tr>
  <td><img src="media/Netflix-Logo.png" style="width: 300px; height: 80px;"/></td>
  <td><img src="media/ebay-logo.png" style="width: 200px; height: 80px;"/></td>
  <td><img src="media/spotify-logo.jpg" style="width: 200px; height: 80px;"/></td>
</tr>
<tr>
  <td><img src="media/reddit.png" style="width: 180px; height: 80px;"/></td>
  <td><img src="media/heineken-beer.jpg" style="width: 130px; height: 80px;"/></td>
  <td><img src="media/snapchat-logo.svg" style="width: 200px; height: 80px;"/><img src="media/pokemon_go_logo.png" style="width: 200px; height: 80px;"/></td>
</tr>
</table>

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

down:

## weitere typische Eigenschaften

* Geografische Verteilung
* Multi-Mandantenfähigkeit
* Hohe Ausfallsicherheit
* Sicherheit: Sicherheitsstandards, Verschlüssellung & Anonymisierung

<img src="media/nelson_question.gif" width="30%" height="30%" class="fragment" data-fragment-index="1"/>

down:

## Service Modelle

NIST Definition: 3 Service Modelle, hierarchisch gegliedert

<img src="media/Service-Model-Pyramid.svg" width="40%" height="40%"/>

down:

## Infrastructure as a Service (IaaS)

* Ist die unterste Schicht des NIST-Service Modells
* Der Cloud-Provider kümmert sich um den Rechenzentrumsbetrieb, Hardware, Netzwerk und Speicher
* Rechenressourcen, Speicher, Netzwerkresourcen werden virtualisiert bereitgestellt
* Durch Virtualisierung kann der Kunde On Demand VM Instanzen bestellen

down:

## Platform as a Service (PaaS)

* mitlere Schicht im NIST Service-Modell
* Der Cloud-Provider stellt die Infrastruktur und eine Cloud-Plattform bereit.
* Die Plattform stellt vorgefertigte Laufzeitumgebungen bereit auf denen die Kundensoftware läuft.
* Es müssen keine VMs gepflegt und betrieben werden, stattdessen kann sich der Kunde um seine Software kümmern.

down:

## Software as a Service (SaaS)

* oberste Schicht im NIST Service Modell.
* Software wird als On-Demand Funktionalität zu jeder Zeit bereitgestellt.
* Der Cloud-Provider verantwortet den gesamten Stack: von Infrastruktur bis zur Applikation.
* Der Kunde ist lediglich nur noch für seine Daten verantwortlich.

down:

### Die Vorteile von Cloud Computing

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

down:

## Virtualisierung

<iframe src='//players.brightcove.net/1534342432001/Byh3doRJx_default/index.html?videoId=3879037056001' allowfullscreen frameborder=0></iframe>
<br>
- VMWare

down:

#### Beispiel: Systemvirtualisierung

<img src="media/virtualization_win_on_osx.png" />
- https://www.virtualbox.org/

down:

#### VMs vs Container

![container-vs-vm](media/container-vs-vms.jpg)

down:

#### Emulation

<img src="media/emulation-example2.png" width="50%" height="50%" />

down:

## Virtualisierung

Frage: Welche Bedeutung hat Virtualisierung für Cloud Computing ?

<div style="white-space: nowrap">
<img src="media/the-thinker.jpg" width="40%" height="40%" />
<img src="media/thinking-monkey.png" width="40%" height="40%" class="fragment" data-fragment-index="1"/>
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

## Auto-Scaling

* Essentieller Mechanismus im Cloud Computing um auf den Bedarf von Ressourcen zu reagieren
* dynamische Bereitstellung von VMs, Container, Speicher, Storage
* bidirektional: Scale-Up, Scale-Down
* Nutzen:
  * Elastizität: bessere Auslastung, Kostenoptimierung (Kosteneinsparung) <!-- .element: class="fragment" data-fragment-index="0" -->
  * Verfügbarkeit und Zuverlässigkeit: durch Sicherstellung von min. Instanzen <!-- .element: class="fragment" data-fragment-index="1" -->
