
## Referatsthemen

- Edge Computing

- Preiskalkulation und Kostenoptimierung bei MS Azure oder Amazon AWS oder Google Cloud

- Cloud Security bei MS Azure oder Amazon AWS oder Google Cloud

- AI-Entwicklung mit der Cloud

- IoT-Entwicklung mit der Cloud

down:

## Referatsthemen

- Cloud-Monitoring

- Migrationsstrategien: von On-Premise in die Cloud

- Serverless Computing

- Datenschutz bei Cloud Computing

- Zertifizierung von Cloud Provider

down:

## Referatsthemen

- Multi-Cloud: Technologien und Betrieb

- Software Entwicklung: Service Meshes

- Cloud-Native Software Entwicklung

- Robotic Process Automation mit Cloud Computing

- DevOps: Software Entwicklung in der Cloud

down:

## Referatsthemen

- Wie funktioniert Dropbox ?

- Wie funktioniert Netflix ?

- Wie funktioniert WhatsApp ?

down:

## Bewertungskriterien

Angemessene Strukturierung des Themas (10Punkte)
- Breite und Tiefeabwägen-Zusammenhang zu Cloud Computing ist gegeben
- inhaltliche Richtigkeit (10Punkte)
- Fach-Terminologien werden richtig angewendet (5Punkte)
- Aktualität: Daten und Quellen sollen aktuell sein (5Punkte)
- Antwort auf Frage zum Thema (5Punkte)

down:

- Formal (5Punkte):
- angemessene Präsentationsform: 
   - kein Ablesen, ansprechender Vortrag
   - kein Abspielen von Videos
   - Quellen-Angabe vollständig und richtig
   - Zeitlimit bei der Präsentation nicht exzessiv überzogen
   - keine Rechtschreibfehler in den Folien

down:

## Coding-Projekt

#### URL Shortener: Beispiel https://bitly.com/

- es soll eine Website mit folgenden Funktionen entwickelt werden:

- eine beliebige URL kann eingegeben werden, die Website gibt eine gekürzte URL zurück
- bei Eingabe der gekürzten URL im Browser, wird an die ursprüngliche URL weiter geleitet

down:

#### URL Shortener

- es können beliebig gleiche URLs eingegeben werden, die Website gibt immer eine andere gekürzte URL zurück, welche zur eingegebenen URL weiterleitet
- eine ungültige URL soll zu einer Fehlermeldung führen
- die gekürzte URL soll im folgenden Format zurückgegeben werden:http://{Servername/Localhost}/{URL-Pfad}, der URL Pfad darf maximal 5-stellen lang sein

down:

#### URL Shortener

Rahmenbedingungen:

- die Programmiersprache kann beliebig gewählt werden
- die Website soll alsDocker Container gestartet werden können
- der Code muss als Git-Repository existieren-eine Anleitung in Form einer README.md Datei soll existieren, darin soll beschrieben sein wie das Docker-Image gebaut werden kann und wie die Website gestartet werden soll

down:

- der Code soll aus folgenden Tests bestehen:
- die Eingabe von 1000 unterschiedlichen URLs führt zu unterschiedlich gekürzten URLs (es darf keine Kollision geben)
- die Eingabe einer eingültigen URL soll zu einem Fehler führen (der Test is bestanden wenn eine ungültige URL zu einem Fehler führt)
- die Länge des URL-Pfades darf nicht größer als 5 sein-mind. 2 weitere Unit-Tests sollen implementiert sein
- es soll in der README.md Datei beschrieben sein, wie die Tests gestartet werden können

down:

## Bewertungskriterien

- Vollständigkeit der Funktionalitäten (20 Punkte)
- keine Bugs (jeder gefundene Bug zählt als -1 Punkt)
- Vollständige Anleitung (5 Punkte)
- Tests sind da (10 Punkte)
- kann eigenständig als Docker Container gestartet werden (5Punkte)
