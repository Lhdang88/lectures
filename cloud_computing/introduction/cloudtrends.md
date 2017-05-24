## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-pulls-stats.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey2.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey3.png)
</div>

down:

## Container Technologie: Docker

<div style="background-color: #ffffff;">
![docker-stats](media/docker-survey4.png)
</div>

down:

## Docker Demo (Teil 2)

App-Containerisierung:

![packaging](media/packaging.gif)

down:

#### Container Orchestrierung

![containers](media/containers.gif)

down:

## Container Orchestrierung

* Framework verantwortlich für Container Life-cycle, Scaling, Networking, Loadbalancing, Virtual Storage
* Container kommunizieren über ein privates Netzwerk miteinander
* Kommunikation nach extern über externes Netzwerk
* "Bring-your-own-Container"-Prinzip: die Plattform startet beliebige Container-Images
* Container Images werden in Image-Repositories hochgeladen (public/private)

down:

Bedeutung für Cloud Computing

* Basis für Container-as-a-Service (CaaS)
  * flexibler als PaaS, einfacher als IaaS
  * CaaS als Alternative zur PaaS und IaaS
  * DevOps-Orientiert
* Kein Vendor Lock-in
  * Kubernetes ist open-source, integrierbar in private / public cloud

down:

Beispiel:

<div class="stretch">
<table>
<tr>
  <td width="40%" height="40%">
    ![Kubernetes](media/kubernetes.png)
    <br>
    [Kubernetes](https://kubernetes.io/)</td>
  <td width="40%" height="40%">
    ![Docker-Swarm](media/docker-swarm.png)
    <br>
    [Docker Swarm](https://docs.docker.com/engine/swarm/)</td>
</tr>
</table>
</div>

down:

## Serverless

![Serverless-Lambda](media/Lambda_HowItWorks.png)

down:

* Serverless != Ohne Server
* kurzlebige Funktionen (stateless)
* In Serverless-Funktionen können On-Demand Rechenoperationen implementiert werden, die nicht ständig laufen müssen
* Lambda-Funktionen werden in der CLoud On-Demand erstellt, ausgeführt und beendet
* Die Kosten werden im Pay-per-Use Prinzip in Millisekunden abgerechnet

down:

Bedeutung für Cloud Computing

* Rechenkosten können genauer abgerechnet werden (Pay-per-Use auf Millisekunden - Basis)
* Rechenkosten entstehen wirklich nur bei Bedarf
* Leichtgewichtige Funktionen können schnell entwickelt und in den Betrieb überführt werden
* Management und Betrieb von Funktionen liegen in der Verantwortung des Cloud-Providers

Beispiele:

AWS Lambda, Apache OpenWhisk, Google Cloud Functions
