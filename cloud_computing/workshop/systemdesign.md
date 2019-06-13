### Aufgabe: System Design

Entwerfe in der Cloud ein System für folgende Anwendungsfälle:

- Online Banking Portal
- URL-Shortner Dienst (tinyURL, bitly)
- Streaming Dienst (Netflix, Spotify)

Wendet das Wissen aus der Vorlesung an (Nutzt Cloud Services) !

down:

### Tips: Fragen und Entscheidungswege

https://github.com/donnemartin/system-design-primer

down:

### Tips: Fragen und Entscheidungswege

Anforderungen, Annahmen sammeln:

- Wer nutzt es (Wie, Wo, Wieviele)
- Was ist die Hauptfunktion des Systems
  - Was sind die Eingaben, was die Ausgaben
  - Sollen Daten permanent gespeichert werden
  - Verhältnis Lese- und Schreib Operationen

down:

### Tips: Fragen und Entscheidungswege

High-Level Architektur / Systementwurf:

- Welche Componenten gibt es ?
- Unterscheidung in
  - Computation, Storage, Communication
- Pseudo APIs entwickeln

down:

### Tips: Fragen und Entscheidungswege

Detailierung:

- Löse Kernprobleme: was ist die Hauptfunktion, wie wird sie gelöst
- Entscheide zwischen Availability und Consistency
- Wie wird Skaliert ?
- Scale-out Mechanismus defnieren: Loadbalancing vs DB Replication vs Sharding vs Caching
