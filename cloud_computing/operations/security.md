### Cloud Computing Sicherheit

* allgemeine Sicherheitsrisiken betreffen auch Cloud Services (Anwendungen)
* durch Verlargerung (Outsourcing) in die Cloud, gibt es mehr Sicherheitsrisiken zu beachten
* potentiell größere Angriffsfläche als im Intranet

down:

### Allgemeine Sicherheitsrisiken

* Netzwerk
  * (D)DoS
  * Man-in-the-Middle, Abhören
  * DNS Hijacking
* Software
  * Exploits (Exploitable Bugs)
  * SQL Injection, Buffer Overflows
  * XSS - Cross-site-scripting, Cross-Site-Token-Forgery
  * Sicherheitslücken in OS, Programmen, Runtime, Protokollen etc.

down:

<div style="background-color: white;">
<img src="media/Heartbleed_bug_explained.png" width="50%" height="50%" />
<img src="media/dns-manipulation.gif" width="50%" height="50%" />
</div>

down:

### Allgemeine Sicherheitsrisiken

* User
  * Unachtsamkeit, unsichere Passwörter
  * Phishing, Spoofing
  * Social Engineering, Scams
* Physisch
  * Naturkatastrophen
  * Stromversorgung, Netzausfall
* Mitarbeiter
  * Spionage, Sabotage
  * Inside Jobs, Malicious Insider
  * Unterbeauftragung, Subunternehmer

down:

<img src="media/phishing.jpg" width="50%" height="50%" /><br>
<img src="media/social-engineering.jpeg" width="50%" height="50%" /><br>
[haveibeenpwnd](https://haveibeenpwned.com/)

down:

### Abwehrstrategien & Maßnahmen

* Compliance
* Security Policies, Awareness
* Security Patches
* Data Encryption, End-to-End Encryption
* Audits, penetration tests

down:

#### Beispiel: Abhören über Http-Kommunikation

* unverschlüsselte Kommunikation (Daten werden im Klartext versendet)
* abhörbar, persönliche Daten, Passwörter können entwendet werden
* Angriffsvektor: z.B. Router-Hijacking

<img src="media/eavesdropping-attack.jpg" width="40%" height="30%" />

down:

#### Gegenmaßnahme: Https-Kommunikation

* Kommunikation über einen verschlüsselten Kanal (Klartext wird zu '%$nO3s;M2d%W')
* SSL/TLS Protokoll
* Basis: symmetrische  + asymmetrische Verschlüsselung

<img src="media/hijacking_https.png" width="40%" height="40%" />

down:

#### SSL/TLS Protokoll (vereinfacht)

* 'Hello'
* Key-Exchange (über asymmetrische Verschlüsselung)
* Starte Verschlüsselungskanal (über symmetrische Verschlüsselung)

down:

#### SSL/TLS Protokoll (vereinfacht)

<div style="background-color: white;">
<img src="media/Simple_SSL_Handshake.svg" width="60%" height="60%" />
</div>

down:

#### Mit wem kommuniziere ich ?

Problem: Man-in-the-Middle

<img src="media/mitm.jpg" width="60%" height="60%" />

down:

#### Authentifizierung mit Zertifikaten

* Zertifikat enthält publick Key
* Certificate Authority (Ausstellungsinstanz) bestätigt Echtheit des Zertifikats und den Kommunikationspartner
* Key-Exchange kann anschließend durchgeführt werden

down:

#### Authentifizierung mit Zertifikaten

<iframe width="560" height="315" src="https://www.youtube.com/embed/i-rtxrEz_E8" frameborder="0" allowfullscreen></iframe>
https://www.youtube.com/embed/i-rtxrEz_E8

down:

weiterführende Erklärung: Chain of trust, https://youtu.be/heacxYUnFHA

<iframe width="560" height="315" src="https://www.youtube.com/embed/heacxYUnFHA" frameborder="0" allowfullscreen></iframe>

down:

#### SSL/TLS Protokoll

<img src="media/ssl_handshake.gif" width="50%" height="50%" />

down:

### Organisationen im Bereich Internet / Cloud Security

* Cloud Security Alliance
  * [Top 12 Cloud Computing Security Threads](https://downloads.cloudsecurityalliance.org/assets/research/top-threats/Treacherous-12_Cloud-Computing_Top-Threats.pdf)
  * <font size="4"> https://downloads.cloudsecurityalliance.org/assets/research/top-threats/Treacherous-12_Cloud-Computing_Top-Threats.pdf </font>

* Open Web Application Security Project
  * [OWASP Top 10](https://www.owasp.org/index.php/Top_10_2017-Top_10)
  * <font size="4">https://www.owasp.org/index.php/Top_10_2017-Top_10</font>

down:

#### Top 12 Cloud Threats
<div>
<font size="6">
<ol>
  <li>Data Breach - Datenleck</li>
  <li>Ungenügende Identity/Credential/Access Management</li>
  <li>Unsichere Schnittstellen / APIs</li>
  <li>Systemlücken, Exploits</li>
  <li>Account Hijacking</li>
  <li>Malicous Insider</li>
  <li>Advanced Persistent Threats (APT)</li>
  <li>Data loss - Datenverlust</li>
  <li>Ungenügende Sorgfalt: Cloud-Strategie</li>
  <li>Missbrauch von Cloud Services</li>
  <li>Denial of Service (DoS)</li>
  <li>Shared Technology Vulnerabilities</li>
</ol>
</font>
</div>

down:

### Cloud Security: Verantwortung

<p>Wer ist verantwortlich für Sicherheit in der Cloud ?</p>
<p class="fragment">Garantiert der Cloud Solution Provider Sicherheit ?</p>
<p class="fragment">Nein, CSP und Cloud Kunde / Nutzer teilen sich die Verantwortung</p>
<p class="fragment">Es kommt auf den Cloud Services, Angriffspotentiale, Sorgfaltspflicht und Wichtigkeit der Daten an</p>

down:

#### CSA - Ungenügender Schutz für Credentials

* Ursachen:
  * ungenügende Security Policy, schwache Passwörter

* Schaden:
  * [Cloud Credentials hosted on Github](https://www.forbes.com/sites/runasandvik/2014/01/14/attackers-scrape-github-for-cloud-service-credentials-hijack-account-to-mine-virtual-currency/#142ca2cf3196)

* Maßnahmen:
  * strengere Security Policy, Audits
  * Multifactor Authentication (MFA), Single-Sign-On (SSO)

down:

#### CSA - Systemlücken, Exploits

* Beispiel:
  * Heartbleed, "WannaCry"-Ransomware

* Maßnahmen:
  * IaaS/CaaS: automatische Security Patches für OS-Kernel, OS-Libraries
  * PaaS: automatische Container Patches und Runtime-Patches
  * SaaS: Patching in der Verantwortung des Cloud Solution Providers

down:

#### CSA - Malicious Insider

* Ursachen:
  * Mitarbeiter (und MA von Subunternehmern) haben ungeschützten Zugriff auf vertrauliche Daten
  * ungenügendes Access Management, physikalische Absicherung, MA Monitoring

* Beispiel:
  * Wikileaks, NSA - Leaks

down:

#### CSA - Malicious Insider

* Maßnahmen:
  * Security Awareness, Access Management
  * MA Screening
  * In Rechnenzentren (Cloud Provider): Sicherheitszonen, Personenschleusen, Biometrische Scanner, verschließbare Racks
  * Datenverschlüsselung

down:

#### CSA - Denial of Service

* Ursachen:
  * böswillige Angriffe durch Konkurrenten, Spione, Hacker
  * "Kundenansturm" (Wie kann man DoS von Überlast unterscheiden ?)

* Angriffsvektor:
  * Infrastruktur: Loadbalancer, Netzwerk
  * Applikation: Functionsüberlastung, DB-Überlastung

down:

#### CSA - Denial of Service

* Maßnahmen:
  * Infrastruktur Absicherung durch Cloud Provider
  * IP/App-based Rate-Limits/Blacklisting durch Cloud Provider / Service Betreiber
  * Microservices (decoupling of applications)
  * Verringerung der Service Qualität

* mehr:
  * <font size="4">https://d0.awsstatic.com/whitepapers/Security/DDoS_White_Paper.pdf</font>

down:

### Auditing: Cloud Zertifizierungen

* Motivation:
  * Kontrolle über Einhaltung von Sicherheitsregeln beim Cloud Provider
  * Vertrauen

* Problem:
  * sehr schwierig da geograph.-verteilt
  * nicht für jeden Kunden umsetzbar

down:

### Cloud Zertifizierungen

* Auditing durch eine Zertifizierungsstelle (3rd Party)
* Einhaltung von Compliance Regeln, Sicherheitspolicies, Sicherheitsstandards
* Technologie-Einsatz, Datenschutz, Organisation, Prozesse
* derzeit keine staatliche Zertifizierungsstelle
* unterschiedliche Standards und Bewertungskriterien mit unterschiedlicher Güte
* Beispiele: ISO 27001, Certified Cloud Service TÜV Rheinland, EuroCloud SaaS Star Audit

<font size="4" />mehr: https://digitalize-your-business.de/zertifizierte-cloud-services-in-deutschland-und-europa-qualitaet-mit-brief-und-siegel/ </font>

down:

#### Searchable Encryption

* Motivation:
  * Verschlüsselung von Daten in der Cloud
  * Ausführung von Suchen auf verschlüsselten Daten

* Ansätze:
  * Deterministic Encryption
  * Symetric Searchable Encryption
  * Asymetric Searchable Encryption
  * Oblivious RAM

* <font size="4" />http://outsourcedbits.org/categories/encrypted-search/ </font>

down:

## Identity Management in der Cloud

* Authentifizierung
  * Logins für verschiedene Personen Gruppen: Anwender, Entwickler, Administratoren, Product Owner
* Autorisierung
  * Accessmanagement für SaaS-Applicationen, VMs für Infrastruktur

down:

### Beispiele

* AWS IAM
  * Gruppen, User, support für Multi-Factor-Authentication
  * Access Management über Security Poilicies (JSON-Files)
  * Resourcen
    * ARN: Amazon Resource Name
    * Actions

down:

### AWS IAM User Management

<iframe width="560" height="315" src="https://www.youtube.com/embed/ySl1gdH_7bY" frameborder="0" allowfullscreen></iframe>
* https://www.youtube.com/embed/ySl1gdH_7bY

down:

### Probleme mit Cloud IDM

* Unternehmen haben meist schon ein zentrales IDM, Ersatz meist unerwünscht
* Yet-another-Username-Password (YAUP) für SaaS-Anwendungen (aus verschiedenen Clouds)
* kein Single-Sign-On
* Gefahr von Vendor Lock-in, wenn ausschließlich IDM des Cloud Providers genutzt wird
* Login Daten liegen in der Cloud

down:

### On-Premise IDM-Integration

* Motivation:
  * IDM soll in der Enterprise IT bleiben
  * keine redundanten user-accounts
  * Kosten Einsparung
  * erhöhte Sicherheit: SSO, 1 Account pro MA, Daten bleiben on-premise

down:

### Enterprise IDM: Windows Active Directory

* Active Directory Protocol
* Identitäten und Rollen: Groups, Users
* Baumstruktur
* SSO im Intranet z.B. durch [Kerberos](https://www.youtube.com/watch?v=kp5d8Yv3-0c), Session Cookies

down:

### Wie kann man SaaS-Anwendungen beibringen Enterprise AD-Usern zu authentifizieren und zu autorisieren ?

down:

### Trust Federation

* Idee:
  * zentraler Identity Provider (IP), authentifiziert User und erstellt ein Auth-Token
  * Services / Apps (Service Providers) sind so konfiguriert dass sie den Identity Provider vertrauen (Federated Trust)
  * Jeder unauthorisierter Zugriff auf einen Service wird an den IP weitergeleitet
  * IP leitet Auth-Token an den Service Provider

* Beispiele: SAML, OpenId

down:

### Protokoll SAML

* Security Assertion Markup Language (SAML)
* Single-Sign-On für die Cloud Integration

<iframe width="560" height="315" src="https://www.youtube.com/embed/i8wFExDSZv0" frameborder="0" allowfullscreen></iframe>
* https://www.youtube.com/embed/i8wFExDSZv0

down:

### Identity Federation

* Idee:
  * die Rollen und Zugriffsberechtigungen sind im Netzwerk / Services verteilt
  * jeder Service verwaltet nur die Berechtigungen die es braucht
  * Authentifizierung geschieht per Trust Federation über den Identity Provider
  * Mapping der Identität des Users auf seine Berechtigungen erfolgt im Service

down:

### MS AD Federation Service

* MS Service für Identity Federation
* kann als Identity Provider für eine Cloud-Integration dienen
* ADFS authentifiziert User gegen On-Premise Enterprise AD
* ADFS generiert SAML Tokens für konfigurierte Trusts (Cloud Services)

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/8xNuPhDVbHU" frameborder="0" allowfullscreen></iframe>
* https://www.youtube.com/embed/8xNuPhDVbHU

down:

### Integration mit MS ADFS + AWS IAM

* Setup: two-way federated trust zwischen ADFS und AWS IAM
* ADFS authentifiziert und erstellt ein authentication ticket in Form eines signiertes SAML-Tokens
* ADFS Rules: überträgt AD Gruppen zu IAM Rollen und speichert diese im SAML Token
* AWS IAM empfängt signiertes SAML-Token und autorisiert Zugriff

down:

### Integration mit MS ADFS + AWS IAM

<img src="media/aws_iam_integration.png" width="80%" height="80%" />

down:

### Integration mit MS ADFS + Azure AD

* Lösungen:
  * Azure AD ist selber ein Identity Provider für Azure mit Unterstützung für Web-IDM Protokolle e.g. SAML, OpenId
    * Azure SaaS Apps können Azure AD als Identity Provider nutzen
    * SSO für Azure SaaS-Apps (auch externe SaaS-Apps: Salesforce)
  * ADFS + AD Connect (ehem. "DirSync") synchronisiert Ids mit Azure AD
  * Azure AD + ADFS authorisieren User

down:

<img src="media/dirsync.png" width="50%" height="50%" />

down:

<iframe width="560" height="315" src="https://www.youtube.com/embed/IcSATObaQZE" frameborder="0" allowfullscreen></iframe>
* https://youtu.be/IcSATObaQZE?t=6m6s

down:

## Identity-as-a-Service (IDaaS)

* Identity Provider für die Cloud
* keine On-Premise Lösung mehr nötig
* Ersatz für Enterprise AD
* SSO für Cloud

down:

## Fragen ?

<img src="media/bleach-question.gif" width="70%" height="70%" />
