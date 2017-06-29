## Gast-Vortrag: Rechenzentrumsbetrieb

* Gast-Redner: M.Sc. Gerrit Schmitz
* Security Expert
* Connected Services, Robert Bosch GmbH
* Dozent DHBW Stuttgart

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/XZmGGAbHqa0" frameborder="0" allowfullscreen></iframe>

down:

# Rechenzentren &amp; Sicherheit

down:

## Was ist ein Rechenzentrum?

down:

<p>Simpel: Ein Raum in dem Informationstechnik betrieben wird.</p>
<p class="fragment">Aber es gibt Qualitätsunterschiede.</p>

down:

## Data Center Tiers

down:

Das Uptime Institute hat schon in den 90ern Rechenzentren anhand ihrer Infrastruktur klassifiziert. Dabei kamen vier aufeinander
aufbauende "Tiers" zustande.<br/>
<a href="https://journal.uptimeinstitute.com/explaining-uptime-institutes-tier-classification-system/">https://journal.uptimeinstitute.com/explaining-uptime-institutes-tier-classification-system/</a>

down:

<dl>
    <dt>Basic Capacity</dt>
    <dd class="fragment">Dedizierter rund um die Uhr klimatisierter Raum mit unterbrechungsfreier Stromversorgung und Generator.</dd>
    <dt class="fragment">Redundant Capacity Components</dt>
    <dd class="fragment">Sowohl Klimaanlage als auch Stromversorgung sind redundant, um Anlagenausfälle abzufangen.</dd>
</dl>

down:

<dl>
    <dt>Concurrent Maintainable</dt>
    <dd class="fragment">Alle Anlagen können gewartet werden, ohne den Betrieb einzuschränken.</dd>
    <dt class="fragment">Fault Tolerance</dt>
    <dd class="fragment">Alle Komponenten und Versorgungspfade können einzeln ausfallen, ohne den Betrieb einzuschränken.</dd>
</dl>

down:

Ein ordentliches Rechenzentrum schaut etwa so aus:
<img src="http://www.google.com/about/datacenters/gallery/images/_2000/CBF_008.jpg" width="70%" height="70%" /><br/>

down:

Mehr Bilder unter
<a href="http://www.google.com/about/datacenters/gallery/#/tech/1">http://www.google.com/about/datacenters/gallery/#/tech/1</a>

down:

Ein einzelnes Rechenzentrumsgebäude bzw. je nach Aufbau auch -stockwerk nennt man im Cloud-Speak Availability Zone.

down:

## Versorgungspfade

down:

Dank der immer fortschreitenden Verkleinerung sind heutzutage nicht mehr m² das Problem, sondern Kühlung (MW) oder Stromversorgung
(kA).

down:

Und auch beim Strom gibt's Unterschiede.

down:

Bei manchen Stromanbietern verläuft die Spannung nicht genau sinusförmig. Das führt zu elektrischem "Verschleiß".

down:

Nahezu alle Geräte transformieren die Wechselspannung intern zu Gleichspannung. Auch da kann man helfen, indem man die verschiedenen
Stromversorgungspfade phasenverschiebt.

down:

## Naturkatastrophen usw.

down:

Aber wie vermeidet man kleinere (Baustelle kappt Strom) und größere Katastrophen (Erdbeben, Feuer, Überflutung)?

down:

Man muss auch das Rechenzentrum selbst redundant machen :) Das heißt dann bei den meisten Cloudanbietern "Region".

down:

## Inhalt

down:

Man kann die verwendete Hardware grob in drei Kategorien aufteilen:<br/>
<ul>
    <li class="fragment">Netzwerk</li>
    <li class="fragment">Storage</li>
    <li class="fragment">Server</li>
</ul>
<p class="fragment">Die Geräte stecken dabei in einem...</p>

down:

### Rack

down:

Ein 60-80cm breiter, etwa 2m hoher Schrank. Üblicherweise aufgeteilt in 42 Höheneinheiten von je 1,75 Zoll und 19 Zoll Breite.
Die Tiefe variiert von 60-120cm. Der Extraplatz kann dabei für saubere Verkabelung oder Türen benutzt werden.

down:

### Netzwerk

down:

    <p>Das Netzwerk muss je nach Bedarf die Daten zwischen den anderen Kategorien transportieren.</p>
    <p class="fragment">Dabei kommen üblicherweise Ethernet mit 1 - 10GBit/s zum Einsatz.</p>
    <p class="fragment">Infiniband kommt aber auch auf bis zu 290 GBit/s.</p>

down:

    Ein typischer Router:
    <img src="http://www.cisco.com/c/dam/en/us/products/switches/ps9441/ps9402/ps12735/nexus_7004_large.jpg" />

down:

    Ein typischer Switch:<br/>
    <img src="http://www.cisco.com/c/en/us/products/switches/nexus-2248tp-ge-fabric-extender/index/_jcr_content/series_data_hero/data-hero-image/data-hero-image-trigger/parsys-for-c26v4/frameworkimage.img.jpg/nexus2248_large_photo.jpg" />

down:

### Storage

Storage bezeichnet Plattensysteme alle Größe und Protokolle. Das können sein:<br/>
    <dl>
        <dt class="fragment">Direct Attached Storage (DAS)</dt>
        <dd class="fragment">Blockstorage für einen Server</dd>
        <dt class="fragment">Storage attached network (SAN)</dt>
        <dd class="fragment">Blockstorage für mehrere Server. z.B. AWS EBS</dd>
        <dt class="fragment">Network Attached Storage</dt>
        <dd class="fragment">Fileshares wie bsp. Volume Services in Cloud Foundry</dd>
    </dl>

down:

    Ein kleines DAS:<br/>
    <img src="https://webobjects2.cdw.com/is/image/CDW/2562753?$product-main$" />

down:

    Ein großes SAN:<br/>
    <img src="http://www.ncegroup.com/assets/images/ibm-xiv.JPG" style="width: 30%; height: 30%" />

down:

### Server

down:

    Server zeichnen sich primär durch CPU (Architektur, Kerne, Takt) und RAM (Anzahl Module, Größe, Takt) aus. Dabei ging der
    Trend immer mehr zum Outsourcen der Platten (siehe Storage) und anderer Komponenten hin.

down:

    Ein klassicher Server:<br/>
    <img src="http://cdn1.itpro.co.uk/sites/itpro/files/2015/05/dl80_gen9_6_x_4.jpg" />

down:

    Ein Blade:<br/>
    <img src="http://www.melius-group.ru/13457-thickbox_default/blejd-server-hp-proliant-bl460c-g9.jpg" />

down:

    Ein Blade Center:<br/>
    <img src="http://www.112it.pl/_productPhoto/641016-B21_15478.jpg" />

down:

## Physische Sicherheit

down:

    <p>Menschen müssen natürlich im Rechenzentrum arbeiten.</p>
    <p class="fragment">In Kolokation können u.U. sogar mehrere Kunden Hardware im eigenen Rack installieren.</p>

down:

    Dafür gibt's es dann spezielle Racks:
    <img src="https://www.racksolutions.eu/media/catalog/product/cache/4//9df78eab33525d08d6e5fb8d27136e95/1/4/141-2470-colocation-rack-01.jpg" style="width: 60%; height: 60%" />

down:

    Die Racks benutzen aber auch reguläre Betreiber, die die Zugänge ihrer Mitarbeiter und Dienstleister gerne strenger regeln.
    <p class="fragment">Dabei erhalten die MA dann nur genau die Schlüssel, die sie benötigen.</p>
    <p class="fragment">Das Ganze geht natürlich auch mit Fingerabdrücken oder Retinascannern.</p>
    <p class="fragment">Sollte der Mechanismus dann noch am Netzwerk hängern, kann man genau feststellen, wer was wann geöffnet hat.</p>

down:

    Dieselbe Sensorik verwendet man natürlich auch für den Zutritt zum RZ selber.
    <p class="fragment">Dabei werden oft auch noch Personenschleusen eingesetzt, um sicherzustellen dass sich auch wirklich jede
        Person authentifiziert.</p>

down:

    <h2>Logische Sicherheit</h2>

down:

    Will sich jetzt ein Cloudkunde von den anderen Kunden abschotten (Mandantenfähigkeit, Noisy Neighbor), greift er in der Regel
    auf dedizierte Systeme zurück.
    <p class="fragment">Das klappt auch ganz gut bei Servern. Entweder Host werden VMs auf vorbestimmter Hardware isoliert bzw. man
        kauft Root-Server.</p>
    <p class="fragment">Warum nicht bei Netzwerk und Storage?</p>

down:

    Platt gesagt: die Hardware ist zu teuer.
    <p class="fragment">Server gibt es für wenige Tausend Euro.</p>
    <p class="fragment">Soviel kostet auch ein Rack-Switch oder kleines DAS,</p>
    <p class="fragment">aber ohne Router und SAN macht Cloud nicht wirklich Spaß.</p>

down:

    Dank Firewall (VPC) und SAN-Zoning kann man aber zumindest Vertraulichkeit und Integrität gewährleisten.
    <p class="fragment">Aber selbst Vorreiter AWS garantiert weder Latenz noch Durchsatz.</p>
    <p class="fragment">Spätestens wenn diese Metriken entscheidend werden, sollte man Colo in Betracht ziehen.</p>

down:

    Dann muss man sich aber auch der Hardwareredundanz bzw. dem -support widmen.
    <p class="fragment">Einerseits kann man versuchen Applikationen vorzugsweise über AZ hinweg zu clustern.</p>
    <p class="fragment">Oder man gönnt sich einen teuren Vertrag mit dem Hersteller, der dann innerhalb von x Stunden Ersatzteile liefern muss.</p>

down:

    Im Bereich der Netzwerkredundanz / -kontrolle gibt es noch sehr speziellen Mechanismus bietet auf WAN-Seite noch das Internet.

down:

    <p>Wenn mann sich seinen eigenen IP-Bereich geleistet hat, kann man den zwischen Internetprovidern wechseln
        bzw. aufteilen (BGP).</p>
    <p class="fragment">Das erlaubt eingehenden Verkehr über die Provider zu verteilen. Ausgehende Verbindungen kann man ja sowieso
        routen, wie man will.</p>

down:

## Fragen ?

<img src="media/bush-questions.gif" width="70%" height="70%" />
