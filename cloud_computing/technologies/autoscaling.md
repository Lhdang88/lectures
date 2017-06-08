## Auto-Scaling

* Essentieller Mechanismus im Cloud Computing um auf den Bedarf von Ressourcen zu reagieren
* dynamische Bereitstellung von VMs, Container, Speicher, Storage
* bidirektional: Scale-Up, Scale-Down
* Nutzen:
  * Elastizität: bessere Auslastung, Kostenoptimierung (Kosteneinsparung) <!-- .element: class="fragment" data-fragment-index="0" -->
  * Verfügbarkeit und Zuverlässigkeit: durch Sicherstellung von min. Instanzen <!-- .element: class="fragment" data-fragment-index="1" -->

down:

#### Autoscaling Strategien

* Reaktiv: Cloud Umgebung beobachtet Kernmetriken (CPU, Memory, Traffic) und reagiert auf Last
* Proaktiv:
  * Scheduling (scheduled scaling): Zeitlich geplante Skalierung auf Basis von Erfahrungswerten
  * Prädiktiv (predictiv scaling): durch Vorhersage auf Basis von prädiktive Analyse

down:

#### Beispiel: Auto-Scaling bei AWS (IaaS)

* CPU, Speicherauslastung, Netzwerk Traffic wird durch AWS EC2 überwacht
* alle Logs/Stdout werden an AWS Cloudwatch übermittelt (Logging/Monitoring-Service)
* AMIs/VMs können zu Auto-Scaling Groups hinzugefügt werden, Konfiguration von Scaling-Plans:
  * Scaling Policies: reaktiv (standard), scheduled-scaling, dynamisch (auf Basis von selbstdefinierten Events/Metriken aus Cloudwatch)
  * min./max. und gewünschte Anzahl an Instanzen

<font size="4">[http://docs.aws.amazon.com/autoscaling/latest/userguide/WhatIsAutoScaling.html](http://docs.aws.amazon.com/autoscaling/latest/userguide/WhatIsAutoScaling.html)</font>

down:

#### Beispiel: Auto-Scaling bei AWS (IaaS)

* Ausführung: auf Basis von Scaling Plans werden AMI Instanzen hinzugefügt / terminiert
* hinzufügen von Instanzen (auf Basis von Launch-Configuration):
  * Instanziierung aus AMI
  * boot-up Phase, Initialisierung, Konfigurierung per Skript (siehe AMI Design Strategien)
  * Anbindung an Cloud-Storage
  * Registrierung ins Virtual Private Cloud (Netzwerk)
  * Registrierung beim Elastic Load-Balancer

down:

#### Beispiel: Auto-Scaling bei AWS (IaaS)

* Status Überwachung: Health-Checking
  * über HTTP-Endpunkt: z.B. /heathcheck
  * healthy flag

down:

#### Beispiel: Auto-Scaling bei Cloud-Foundry (PaaS)

* Monitoring / Überwachung von Basis-Metriken: analog zu AWS EC2
* Skalierung auf Container / App-Ebene
* Skalierung über Einbinden eines "Auto-Scaler"-Services an einer App
* Definition von Basis-Metriken:
  * min./max. Instanzen
  * CPU-, Traffic-, Speicher-Grenzen
* nur reaktiv

down:

#### Beispiel: Auto-Scaling bei Cloud-Foundry (PaaS)

* Ausführung: auf Basis der Auto-Scaler Konfiguration werden Container-Intanzen hinzugefügt / terminiert
* hinzufügen von Instanzen:
  * Container Instanz wird aus dem gebautem Image instanziiert
  * Einbinden der Container Instanz ins private virtual network
  * Container Prozess wird gestartet (run-Befehl)
  * Registrierung beim Load-Balancer

down:

#### Beispiel: Auto-Scaling bei Cloud-Foundry (PaaS)

* Status Überwachung: Health-Checking
  * über HTTP-Endpunkt: z.B. /heathcheck, (http-response-Code: 200 bedeutet "OK", ansonsten "NOK")
  * Überwachung des Container Prozesses: terminiert der Container Prozess, stoppt der Container und crasht, es wird ein neuer Container gestartet

down:

#### Beispiel: Auto-Scaling bei Kubernetes (CaaS)

* Monitoring / Überwachung von Basis-Metriken: analog zu Cloud Foundry
* Skalierung auf Pod-Ebene (Kubernetes Konzept: funktional zusammengehörige Menge von Containern)
* Skalierung über die Definition einer Auto-Scaling Konfiguration
* Auto-Scaling Konfiguration wird über Selektoren auf Kubernetes Bausteine (Pod, ReplicaSets, Deployments) angewendet
* Auto-Scaling ist reaktiv und basiert nur auf CPU-Last-Grenzen

down:

#### Beispiel: Auto-Scaling bei Kubernetes (CaaS)

* Ausführung: auf Basis der Auto-Scaler Konfiguration werden Container-Intanzen hinzugefügt / terminiert
* hinzufügen von Instanzen:
  * Pod Instanz wird erstellt, alle Container Definitionen werden aus dem konfiguriertem Image instanziiert
  * Einbinden der Pod/Container Instanz ins private virtual network
  * Container Prozess wird gestartet (run-Befehl)
  * Registrierung beim Service und Load-Balancer

down:

#### Beispiel: Auto-Scaling bei Kubernetes (CaaS)

* Status Überwachung: Health-Checking
  * über HTTP-Endpunkt: z.B. /heathcheck, (http-response-Code: 200 bedeutet "OK", ansonsten "NOK")
  * Überwachung der Pod/Container Prozesse: terminiert der Pod/Container Prozess, stoppt der Pod/Container, es wird ein neuer Pod/Container gestartet
