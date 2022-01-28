## Horizontal Auto-Scaling

* Essentieller Mechanismus im Cloud Computing um auf den Bedarf von Ressourcen zu reagieren
* dynamische Bereitstellung von VMs, Container, Speicher, Storage
* bidirektional: Scale-out, Scale-In

down:

#### Autoscaling Strategien

* Reaktiv: ein "Auto-Scaling"-Dienst beobachtet Metriken (CPU, Memory, Request/s etc.) und skalliert wenn Grenzwerte überschritten werden
* Proaktiv:
  * Scheduling (scheduled scaling): Zeitlich geplante Skalierung
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

#### Keda: Auto-Scaling Erweiterung für Kubernetes

<img src="media/keda-feats.png" width="70%" height="70%"/>

<p>
<font size="4">https://keda.sh/</font>

down:

#### Keda: Auto-Scaling Erweiterung für Kubernetes

<img src="media/keda-arch.png" width="70%" height="70%"/>

<p>
<font size="4">https://keda.sh/</font>

down:

#### Vorteile durch Autoscaling

* Elastizität: bessere Auslastung, Kostenoptimierung (Kosteneinsparung) <!-- .element: class="fragment" data-fragment-index="0" -->
* Verfügbarkeit und Zuverlässigkeit: durch Sicherstellung von min. Instanzen <!-- .element: class="fragment" data-fragment-index="1" -->
