## Liefermodelle

Die NIST Cloud Computing Definition definiert 4 Liefermodelle:

1. Public Cloud
1. Private Cloud
1. Hybrid Cloud
1. Community Cloud

note: * Was bedeutet Liefermodell ? Keine bestimmte Bedeutung, ist hier im Kontext zu verstehen
* Wie wird die Cloud dem Nutzer zugänglich gemacht.

down:

## Public Cloud

<div style="text-align: left;">
Die Cloud ist für alle über das Internet zugänglich.<br>
<br>
Die Infrastruktur wird durch einen (evtl. auch durch mehrere) Cloud-Provider betrieben.
</div>

down:

<img src="media/public-cloud.svg" width="50%" height="50%" style="background-color: white;" />

down:

#### Beispiele:

* [Amazon Web Service](https://aws.amazon.com/)
* [Microsoft Azure](https://azure.microsoft.com/)
* [Google Cloud Platform](https://cloud.google.com/)
* [Telekom Cloud](https://cloud.telekom.de/)

down:

## Public Cloud - Vorteile/Nachteile

<div style="text-align: left;">
+ keine Total Cost of Ownership (TOC)<br>
+ keine Up-front Kosten, Pay-per-Use<br>
+ Mobilität, Kunden können von überall zugreifen<br>
+ Skalierbarkeit und Verfügbarkeit (99,9X %)<br>
+ Globale Präsenz von internationalen Anbietern<br>
<br>
- Kontrollverlust, Intransparente Datenspeicherung<br>
- Keine Anpassungen von Services möglich
</div>

note: * potentieller Nachteil.: keine offiziellen SLAs bei AWS für Services

down:

## Private Cloud

<div style="text-align: left;">
Die Cloud ist nur für einen bestimmten Personenkreis (Organisation, Unternehmen) zugänglich. <br>
<br>
Die Kunden sind die eigenen Geschäftsbereiche oder Abteilungen.<br>
</div>

down:

<img src="media/private-cloud.svg" width="50%" height="50%" style="background-color: white;" />

down:

## Private Cloud - Vorteile/Nachteile

<div style="text-align: left;">
+ Datenkontrolle, die Daten bleiben im Unternehmen<br>
+ Mobilität, Zugriff von Überall (über VPN) möglich<br>
+ Anpassbarkeit der Services<br>
+ keine Standort-Abhängigkeit wie bei Public Cloud<br>
<br>
- Up-front Kosten, Total Cost of Ownership durch Hardware, Rechenzentren, Personal<br>
- Skalierbarkeit der Cloud liegt in der eigenen Verantwortung, keine "unendlichen" Hardware Ressourcen
</div>

down:

## Hybrid Cloud

<div style="text-align: left;">
Einzelne Teile der Cloud können öffentlich und andere teile nur durch spezifische Personenkreise zugegriffen werden.<br>
<br>
Die Infrastruktur kann ein Unternehmen kommplett oder teilweise On Premise hosten, oder aber auch gemeinschaftlich mit einem externen Dienstleister hosten.
</div>

down:

<img src="media/hybrid-cloud.svg" width="50%" height="50%" style="background-color: white;" />

note: * Gründe für Hybrid Cloud, Architektur von Hybrid Cloud

down:

## Hybrid Cloud - Vorteile/Nachteile

<div style="text-align: left;">
+ vereint die Vorteile von Public und Private Cloud<br>
<br>
- Up-front Kosten, Total Cost of Ownership durch Hardware, Rechenzentren, Personal<br>
- Komplexität steigt: IT-Strukturen & Security, Data Governance
</div>

down:

## Community Cloud

<div style="text-align: left;">
Die Cloud wird für verschiedene Personenkreise (verschiedene Unternehmen) einer bestimmten Community (Strategische Partnerschaft) bereitgestellt.<br>
<br>
Die Kunden kommen aus verschiedenen Organisationen und haben dedizierten Zugriff auf die Cloud.<br>
<br>
Die Infrastruktur kann On Premise oder Off Premise gehostet werden.<br>
<br>
Der Betrieb kann dediziert durch eine Partei oder gemeinschaftlich erfolgen.<br>
</div>

down:

<img src="media/community-cloud.svg" width="50%" height="50%" style="background-color: white;" />

note: * gemeinsame Ziele, gleiche Domäne

down:

## Community Cloud - Vorteile/Nachteile

<div style="text-align: left;">
+ analog zu Private Cloud<br>
+ die Gesamtkosten werden durch die Community getragen<br>
<br>
- Up-front Kosten, Total Cost of Ownership durch Hardware, Rechenzentren, Personal<br>
- schwierigere Data Governance, wer darf auf welche Daten zugreifen ? Wo werden Daten gespeichert ?<br>
</div>

down:

## Hosting Varianten

<a href="http://dailyitproblems.azurewebsites.net/wp-content/uploads/2013/12/Cloud_Hostingvarianten_v3.png"><img src="media/Cloud_Hosting.png" width="40%" height="40%"/>
</a>
<br>
<font size="4">
Quelle: http://dailyitproblems.azurewebsites.net/wp-content/uploads/2013/12/Cloud_Hostingvarianten_v3.png, Stand Mai.2017
</font>

note: * Begriffe - on-premise, off-premise erklären
* hosted / managed erklären
* Unternehmen fangen gerne mit Private Cloud Lösungen an und bieten SaaS Lösungen public an -> Hybrid Cloud

down:

## Aufgabe

Erläutere die Begriffe 'Multi Tenancy', 'Availability Zones', 'Elastic Computing' im Kontext von Cloud Computing.
Beschreiben Sie Funktion(sweise), Bedeutung aus Kundensicht/Provider-Sicht. Vergleichen Sie mit klassischen Hosting Diensten e.g. Strato

30 min.