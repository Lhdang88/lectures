## Datenschutz

Darf ich Daten erheben und bei einem Cloud-Provider speichern der nicht in D (oder EU) ansässig ist?

down:

### Datenschutz

* Recap: Besonderheiten bei Cloud Computing
  * keine technische Beschränkung durch natürliche Grenzen
  * Undurchsichtigkeit der Datenverarbeitung
  * Geographische Verteilung, Grenzüberschreitender Datenverkehr
  * Kosteneinsparung durch Übertragung von Verantwortung

down:

### Welche Daten sind schutzbedürftig ?

* Beispiele:
  * Steuerlich relevante Daten (§146 Abs. 2 S1 AO)
    * müssen im Inland oder in einem Mitgliedstaat der EU/EWR (durch Einwilligung der zust. Finanzbehörde) gespeichert werden (§146 Abs. 2a AO)

down:

* Handelsdaten z.B. Buchungsbelege, Handelsbriefe (§257 Abs.4 HGB)
  * müssen im Inland für 6 bzw. 10 Jahre aufbewahrt werden
* Personenbezogene Daten (§3 Abs.1 BDSG)
    * Vertraulichkeit und Integrität muss bewahrt sein

* Quelle:
<font size="4">https://www.datenschutzzentrum.de/cloud-computing/20100617-cloud-computing-und-datenschutz.html</font>

down:

#### Was sind Personenbezogene Daten ?

* §3 Abs. 1 BDSG:
  * "(1) Personenbezogene Daten sind Einzelangaben über persönliche oder sachliche Verhältnisse einer bestimmten oder bestimmbaren natürlichen Person (Betroffener)"
  * Daten die eindeutig einer Person zugeordnet werden können

down:

#### Was sind Personenbezogene Daten ?

  * die Identität einer Person aus dem Inhalt des Datums oder mit Zusatzwissen sich herstellen lässt
* Quellen:
  * <font size="4">https://www.gesetze-im-internet.de/bdsg_1990/__3.html</font>
  * <font size="4">https://www.ldi.nrw.de/mainmenu_Datenschutz/Inhalt/FAQ/PersonenbezogeneDaten.php</font>

down:

#### Was sind Personenbezogene Daten ?

* Beispiele:
  * Alter, Augenfarbe, Geburtsort
  * Telefonnummer, E-Mail Adresse
  * KFZ-Kennzeichen

down:

#### besonders schutzwürdige Personenbezogene Daten
  * "(9) Besondere Arten personenbezogener Daten sind Angaben über die rassische und ethnische Herkunft, politische Meinungen, religiöse oder philosophische Überzeugungen, Gewerkschaftszugehörigkeit, Gesundheit oder Sexualleben"
  * Verlust kann erhebliche Konsequenzen für die betroffene Person haben
  * es gelten erhöhte Schutzmaßnahmen

down:

### Anwendbarkeit

* anonymisierte Daten
  * BDSG findet keine Anwendung wenn die Daten so anonymisiert sind dass nur mit unverhältnismäßigem Aufwand die Daten einer Person zugeordnet werden können
* pseudonymisierte Daten
  * schließen die Anwendbarkeit des BDSG nicht aus

down:

### Anwendbarkeit

* zentrale Bedeutung hat die "verantwortliche Stelle" (Person die Daten für sich selbst erhebt und verarbeitet bzw. für sich verarbeiten lässt)
* befindet sich diese in der EU/EWR oder Deutschland findet das jeweilige Nationale Recht bzw. deutsches Datenschutzrecht Anwendung
* befindet sich die verantwortliche Stelle außerhalb der EU/EWR, aber werden Daten innerhalb der EU (Server) verarbeitet gilt das "Territorialprinzip"

down:

### Anwendbarkeit

* Sitzlandprinzip (europäisches Recht)
  * Europ. Datenschutzrichtlinie (EU-DSRL) Art. 4 Abs. 1a), b): kommt es für die Anwendbarkeit einzelstaatlichen Rechts darauf an, in welchem Mitgliedstaat die Daten verarbeitende Niederlassung ihren Sitz hat.

down:

* findet Anwendung bei grenzüberschreitenden Datenverkehr, regelt welches Nationale Recht Anwendung findet
* befindet sich eine Niederlassung eines Unternehmens/verantwortliche Stelle in Deutschland (und der Hauptsitz in der EU), in dem die Datenerhebung/-Verarbeitung stattfindet, dann findet das BDSG Anwendung
* Relevant ist das Land in dem sich die Niederlassung der verantwortlichen Stelle befindet, das jeweilige Nationale Recht gilt

down:

### Anwendbarkeit

* Territorialprinzip
  * das jeweilige Nationale Recht findet Anwendung in der die Datenerhebung, -verarbeitung, -nutzung stattfindet, d.h. in dem Land an dem sich die Server befinden


* Quelle:
<font size="4">https://www.datenschutzbeauftragter-info.de/ist-das-bundesdatenschutzgesetz-bdsg-im-internationalen-datenschutz-anwendbar/</font>

down:

### Auftragsdatenverarbeitung

Welche Regelungen gibt es damit Daten zur Verarbeitung in eine Cloud transferiert werden können ?

down:

### Auftragsdatenverarbeitung (§11 BDSG)

* betrifft das Outsourcing von Datenverarbeitung
* regelt die Verantwortlichkeit im Sinne des Datenschutzes, zwischen dem Auftraggeber und Auftragsnehmer
* Verantwortlich ist der Auftragsgeber der die Datenverarbeitung für sich durchführen lässt
* der Auftragsgeber ist die verantwortliche Stelle, hat Kontrollpflichten ggü. dem Auftragsnehmer
* bei Datenverlust/Leck hat die verantwortliche Stelle eine Meldepflicht

down:

### Beispiel Cloud Computing: SaaS

* Rollen: Cloud-Nutzer (Person o. Firma), Cloud Anbieter, Rechenzentrumsbetreiber
* Verantwortliche Stelle ist der Cloud Nutzer, dieser lässt über Auftragsdatenverarbeitung personenbezogene Daten durch den Cloud Anbieter und Rechenzentrumsbetreiber (Subbeauftragung) verarbeiten
* der Cloud Nutzer ist verantwortlich für den Schutz der Daten
* der Cloud Nutzer hat die Pflicht den Cloud Provider sorgfältig auszuwählen

down:

### Mindestanforderungen für die Auftragsdatenverarbeitung
<div style="text-align: left;">
<font size="4">
1. Gegenstand und Dauer des Auftrags<p>
2. Umfang, Art und Zweck der Verarbeitung, Art der Daten und Kreis der Betroffenen<p>
3. die Datensicherungsmaßnahmen nach § 9 BDSG<p>
4. Berichtigung, Löschung und Sperrung der Daten<p>
5. die (Kontroll-)Pflichten der Auftragnehmer (AN)<p>
6. Unterauftragsverhältnisse<p>
7. Kontrollrechte der Auftraggeber (AG)<p>
8. Mitteilungspflichten der AN bei Verstößen<p>
9. Weisungsbefugnisse<p>
10. Datenlöschung beim AN. Nach § 11 Abs. 2 S. 4, 5 BDSG muss sich der AG regelmäßig über die Beachtung der Datensicherungsmaßnahmen überzeugen
</font>
</div>

down:

#### Verarbeitung von personenbezogenen Daten außerhalb der EU
<div style="text-align: left;">
<font size="5">
- nach BDSG nur erlaubt wenn die Einwilligung aller Betroffenen eingeholt wurde oder ein angemessenes Datenschutzniveau im Drittland sichergestellt ist (§ 4b Abs. 2, 3 BDSG)<p>
- angemessenes Datenschutzniveau besteht nach Attestierung der Europ. Kommission in Andorra, Argentinien, Australien, Faroer Inseln, Guernsey, Israel, Isle of Man, Jersey, Kanada, Schweiz, Uruquay und Neuseeland<p>
- für die Nutzung in Staaten außerhalb der EU muss ein angemessenes Datenschutzniveau gewährleistet werden, z.B. durch gesonderte Abkommen:<p>
- Bsp.: Safe-Harbor (nicht ausreichend), Binding Corporate Rules (muss durch die Datenschutzaufsichtsbehörden genehmigt werden)
</font>
</div>

down:

### Fazit
<div style="text-align: left;">
<font size="5">
- Es ist am sichersten dass Daten die innerhalb der EU erhoben/verarbeitet werden, die EU Grenzen nicht verlassen <p>
- als Maßnahmen zur Erfüllung der Kontrollpflicht als verantwortliche Stelle können Zertifizierungen des Cloud Providers herangezogen werden (ISO 27001, Trusted Cloud) <p>
- neben des Standorts, sollte der Cloud Provider sorgfälltig nach folgenden Kriterien ausgesucht werden: <p>
- Verschlüsselungsmöglichkeiten, Anonymisierung von Daten <p>
- werden Daten in ein Drittland repliziert ? <p>
- Verbindliche Zusagen in Sachen Transparenz, SLAs, Vertragliche Zusagen ausreichend? (z.B. Mindestanforderungen für ADV) <p>
</font>
</div>
