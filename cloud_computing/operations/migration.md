## Cloud Migration

Welcher Weg führt in die Cloud ?

down:

### Gründe Cloud Computing

- Kostenreduktion
- Skallierbarkeit
- Agilität
- Innovation
- Verfügbarkeit
- Sicherheit

down:

### Häufig gestellte Fragen

- Welche Risiken birgt die Cloud ?
- Wieviel Kontrolle wird abgegeben ?
- Welcher Aufwand steckt hinter einer Migration ?
- Welche Personen und welche Fähigkeiten werden gebraucht ?
- Welche Cloud zum Business case ?
- Was soll in die Cloud wandern ?

down:

### Kriterien für eine Evaluation

Risiken

- Datenschutz, Auftragsdatenverarbeitung, SLAs usw.
- Kontrollverlust & Abhängigkeit, wie schnell reagiert der Cloud Provider ?
- Kultureller Wandel: Oranisationsänderung
- Sicherheit - Habe ich ein Sicherheitskonzept ?
- Kosten - Cloud als Kostenfalle ? Effiziente Nutzung Möglich ?

down:

### Kriterien für eine Evaluation

Bedarfsermittlung

- Welcher Anteil meiner IT soll in die Cloud ?
- Welche Kosten möchte ich sparen ?
- Welchen Vorteile von Cloud Computing möchte ich nutzen ?

down:

### Kriterien für eine Evaluation

Aufwandsabschätzung

- Welche Fähigkeiten werden benötigt ?
- Welche Organisatorischen Veränderungen werden erforderlich ?
- Was kostet eine Migration ?
- Wieviel Zeit wird benötigt ?

down:

### Guidelines für die Migration

Google Cloud Adoption Framework
<p>
<font size="4">https://cloud.google.com/adoption-framework</font>
<p>
Azure Cloud Migration Strategy
<p>
<font size="4">https://azure.microsoft.com/de-de/migration/migration-journey/#get-started</font>
<p>
AWS Migration Whitepaper
<p>
<font size="4">https://docs.aws.amazon.com/whitepapers/latest/aws-migration-whitepaper/welcome.html</font>

down:

### Migration Strategie: 6R's

<img src="media/6rmigration.png" width="75%" height="65%"/>
<br>
<font size="4">https://docs.aws.amazon.com/whitepapers/latest/aws-migration-whitepaper/the-6-rs-6-application-migration-strategies.html</font>

down:

### Migration Strategie: 6R's

Rehosting

- Cloud Migration ohne Veränderung an Software
- Umstellung des Betriebs von On-Prem zu Cloud, durch Nutzung von IaaS
- Vorteil: Schnelle Migration
- Nachteil: keine automatische Skallierbarkeit, Cloud Potential wird nicht ausgeschöpft

down:

### Migration Strategie: 6R's

Replatforming

- Bestimmte Komponenten werden in der Cloud durch managed-services ausgetauscht
- Bspw. Datenbanken, Message Queues, Loadbalancer, Cloud-Speicher
- Vorteil: Aufwand gering, Kostenreduktion möglich durch weniger Wartung und Betrieb durch managed Services
- Nachteil: Skallierbarkeit, Cloud Potential nicht vollständig ausgeschöpft

down:

### Migration Strategie: 6R's

Repurchasing

- Wechsel von On-Premise Lösung auf Saas
- Vorteil: geringer Aufwand, Kostenreduktion durch weniger Wartung und Betrieb, Skallierbarkeit
- Nachteil: ggfs. Vendor Lock-in

down:

### Migration Strategie: 6R's

Refactoring

- Umbau der On-Premise Software in eine Cloud Native Software
- Nutzung von PaaS und managed Services
- Vorteil: volles Potential der Cloud wird genutzt, Skallierbarkeit
- Nachteil: hoher Aufwand, benötigt viel Know-how

down:

### Migration Strategie: 6R's

Retain
- Cloud Migration wird nicht durchgeführt
- Vorteile der Cloud überwiegend z.B. nicht den Aufwand, Nutzen ist gering

Retire
- der Betrieb wird eingestellt, der Nutzen der Software ist nicht mehr vorhanden

down:

### Migration Strategie: 6R's

<img src="media/grad-adoption.png" width="75%" height="65%"/>
<br>
<font size="4">https://www.adesso.de/de/news/blog/gruende-und-strategien-fuer-die-migration-einer-applikation-in-die-cloud.jsp</font>

down:

### Other names ...

Lift and Shift
- wie Rehosting: Migration in die Cloud mit keiner/bis wenig Änderung

Improve and Move
- Refactoring während der Migration, um Cloud Potential besser auszuschöpfen.
- Bspw. Auslagerung von "States" in eine Datenbank/Cache, um eine App besser skalieren zu können

down:

Rip and Replace

- komplette Neu-Implementierung in eine Cloud Native App

<font size="4">https://cloud.google.com/solutions/migration-to-gcp-getting-started#types_of_migrations</font>

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Bghvb9eMrss" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<font size="4">https://youtu.be/Bghvb9eMrss</font>

down:

#### Cloud Computing im Unternehmen etablieren

<img src="media/googlemigration.png" width="75%" height="65%"/>
<br>
<font size="4">https://cloud.google.com/solutions/migration-to-gcp-getting-started#gcp_adoption_framework</font>

down:

#### Cloud Computing im Unternehmen etablieren

<img src="media/googlemigration2.png" width="75%" height="65%"/>

- Assess: welche Apps sollen migriert werden ? Welche Abhängigkeiten ? Potentielle Kosteneinsparungen ermitteln

- Plan: migrationsstrategie erarbeiten: 6R, sicherheitskonzept planen, Organisation und Projekt struktur planen

down:

- Deploy: Migration durchführen, iterativ nachsteuern

- Optimize: Cloud Potential ausschöpfen, Bspw. fortgeschrittene Themen wie: Disaster Recovery, Kostenoptimierung, Automatisierung

down:

#### Wichtige Schritte während der Migration

- kennenlernen der Cloud in kleinen Teams
- Proof-of-Concepts durchführen
- Risikobewertung, Kosten/Nutzen evaluieren

down:

#### Wichtige Schritte während der Migration

- Cloud Governance Team etablieren
- Sicherheitskonzept erarbeiten
  - Identity Management, Rechtemanagement
  - Netzwerkplanung
  - Security Policies
- Migrationsplan / Template erarbeiten

down:

#### Wichtige Schritte während der Migration

- Budget-Pläne, Kosten Monitoring
- Cloud Onboarding Programme entwickeln
- Cloud Nutzung Optimieren