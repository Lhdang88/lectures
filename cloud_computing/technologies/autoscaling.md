## Horizontal Auto-Scaling

* Essentieller Mechanismus im Cloud Computing um auf den Bedarf von Ressourcen zu reagieren
* dynamische Bereitstellung von VMs, Container, Speicher, Storage
* bidirektional: Scale-out, Scale-In

down:

#### Autoscaling Strategien

* Reaktiv: Cloud Umgebung beobachtet Kernmetriken (CPU, Memory, Traffic) und reagiert auf Last
* Proaktiv:
  * Scheduling (scheduled scaling): Zeitlich geplante Skalierung auf Basis von Erfahrungswerten
  * Prädiktiv (predictiv scaling): durch Vorhersage auf Basis von prädiktive Analyse

down:

#### Beispiel: Auto-Scaling bei Kubernetes

* auf Pod-Ebene (Container): Horizontal Pod Autoscaler, Vertical Pod Autoscaler
* auf Node-Ebene (VMs): Cluster Autoscaler

<p>
<font size="4">https://medium.com/better-programming/build-kubernetes-autoscaling-for-cluster-nodes-and-application-pods-bb7f2d716b07</font>
<p>
<font size="4">https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale</font>

down:

#### Beispiel: Horizontal Pod Autoscaler (HPA)

* Monitoring von Basis-Metriken: CPU und Mem
* Skalierung auf Pod-Ebene (min/max Pod Instanzen)
* Skalierung über die Definition einer HPA Konfiguration
* Auto-Scaling ist reaktiv und basiert Über-/Unterschreitung von CPU-Last-Grenzen

down:

#### Beispiel: Auto-Scaling bei Kubernetes

* Scale-out - Hinzufügen von Instanzen:
  * Pod Instanz wird aus dem Pod-Template instanziiert
  * Container Prozess wird gestartet (run-Befehl)
  * Umgebungsvariablen werden gesetzt
  * Volumes (Speicher) werden eingebunden
  * Private virtual network wird eingebunden
  * Registrierung beim Service und Load-Balancer

down:

#### Beispiel: Auto-Scaling bei Kubernetes

* Status Überwachung: Health-Checking
  * über HTTP-Endpunkt: z.B. /heathcheck, (http-response-Code: 200 bedeutet "OK", ansonsten "NOK")
  * Überwachung der Pod/Container Prozesse: terminiert der Pod/Container Prozess, stoppt der Pod/Container, es wird ein neuer Pod/Container gestartet

down:

#### Beispiel: Auto-Scaling bei AWS (IaaS)

* CPU, Speicherauslastung, Netzwerk Traffic wird durch AWS EC2 überwacht
* alle Logs/Stdout werden an AWS Cloudwatch übermittelt (Logging/Monitoring-Service)

<font size="4">[http://docs.aws.amazon.com/autoscaling/latest/userguide/WhatIsAutoScaling.html](http://docs.aws.amazon.com/autoscaling/latest/userguide/WhatIsAutoScaling.html)</font>

down:

* VMs können zu Auto-Scaling Groups hinzugefügt werden, Konfiguration von Scaling-Plans:
  * Scaling Policies: reaktiv (standard), scheduled-scaling, dynamisch (auf Basis von Metriken aus Amazon SQS, Cloudwatch alarms)
  * min./max. und gewünschte Anzahl an Instanzen

<font size="4">[https://docs.aws.amazon.com/autoscaling/latest/userguide/as-using-sqs-queue.html](https://docs.aws.amazon.com/autoscaling/latest/userguide/as-using-sqs-queue.html
)</font>

down:

#### Beispiel: Auto-Scaling bei AWS (IaaS)

* Ausführung: auf Basis von Scaling Plans werden VM Instanzen hinzugefügt / terminiert
* hinzufügen von Instanzen (auf Basis von Launch-Configuration):
  * Instanziierung aus Amazon Machine Images
  * boot-up Phase, Initialisierung, Konfigurierung per Skript (siehe AMI Design Strategien)
  * Anbindung an Cloud-Storage
  * Registrierung ins Virtual Private Cloud (Netzwerk)
  * Registrierung beim Elastic Load-Balancer

down:

#### Vorteile durch Autoscaling

* Elastizität: bessere Auslastung, Kostenoptimierung (Kosteneinsparung) <!-- .element: class="fragment" data-fragment-index="0" -->
* Verfügbarkeit und Zuverlässigkeit: durch Sicherstellung von min. Instanzen <!-- .element: class="fragment" data-fragment-index="1" -->
