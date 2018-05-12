## Workshop Session: Crash-kurs NodeJS

<img src="media/nodejs.svg" width="50%" height="50%" /><br>

[https://nodejs.org/en/](https://nodejs.org/en/)

down:

## Ziel

* Erstellung eines Hello-World-Microservices
* Erstellung einer HTTP-API
* Daten speichern in MongoDB

down:

## Werkzeuge

* NodeJS
* Docker
* MongoDB

down:

#### Aufgabe 1

Erstellt ein NodeJS Hello-World Programm:

* node index.js [name] -> 'Hello World, by [name]'

down:

#### Aufgabe 2

Erstellt einen Web-Server mit NodeJS + Express:

* node index.js -> Startet den Web-Server mit Port 80
* GET Request auf /api/hello -> Response mit 'Hello World'

down:

#### Aufgabe 3

Erstellt eine RESTful API für 'CarData' mit Swagger

* RESTful API URI: /api/cardata
* erstellt für die API eine Swagger API Definition
* CarData, soll folg. Informationen enthalten: Auto-Typ, Auto-Marke, Kennzeichen

down:

##### Aufgabe 4

Persistiert 'CarData' in MongoDB

* 'CRUD'-Operationen für 'CarData'