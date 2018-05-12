## Workshop Session: Docker & Kubernetes

<img src="media/docker.jpg" width="250px" height="250px" /><img src="media/kubernetes.png" width="250px" height="250px" /><br>

[https://www.docker.com](https://www.docker.com) <br>
[https://kubernetes.io/](https://kubernetes.io/)

down:

## Ziel

* Erstellung eigener Docker Container
* Betrieb von Docker Container in der Cloud

down:

## Werkzeuge

* Docker (docker)
* Azure CLI (az)
* Kubernetes CLI (kubectl)

down:

#### Aufgabe 1

Erstellt ein Docker Image für die Hello-World App:

* docker run --name hello world -p 80:80 -it hello-world-app

down:

#### Aufgabe 2

Betreibt die Hello-World App im MS Azure AKS Cluster:

* die App soll über das Internet zugreifbar sein
* RESTful API soll 'CarData' in MongoDB abspeichern

down:

#### Aufgabe 3

Betreibt die Hello-World App als MS Azure Function:

* die App soll über das Internet zugreifbar sein
* alle bisherigen RESTful API functions sollen implementiert werden