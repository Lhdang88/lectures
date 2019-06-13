## Workshop: Container-as-a-Service

Agenda:

- Containerizing Apps
- Kubernetes Basics
- Auto-Scaling with Kubernetes

down:

### Containerizing Apps

requirements: 
- Docker (or VM + Docker)
- Docker commands (build, run, ps, stop etc.)

links: 
- https://docs.docker.com/install/linux/docker-ce/ubuntu/
- https://docs.docker.com/engine/reference/commandline/build/
- https://github.com/wsargent/docker-cheat-sheet

down:

### Task 1 (60 min.)

Create a Web-app, that provides an URL-Endpoint /prime that calculates whether a given number (Integer) is a prime or not.

example: 
```
Http-Request GET at "http://example.foo.bar/prime?number=5"
```
returns 

```
    {"message":"5 is a prime","isPrime":true,"calcTime":"2 ms"}
```

down:

### Task 1 (60 min.)

implement in any language you want !

Afterwards 'containerize' it with Docker

down:

### Kubernetes Basics

https://kubernetes.io/

down:

### Deployment types

- 'Bring-Your-Own-Code'
- 'Bring-Your-Own-Container'

down:

### Deployment with Kubernetes

requirements:

- Kubernetes Cluster
- kubectl CLI
- deployment - definitions (e.g. yaml-files)

links:
- https://kubernetes.io/docs/reference/kubectl/cheatsheet/#viewing-finding-resources

down:

### Auto-Scaling with Kubernetes

Auto-Scaling basics ...

down:

### Auto-Scaling with Kubernetes

Horizontal Pod Auto-Scaler

- https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/

down:

### Task 2: Let Kubernetes auto-scale (60 min.)

- build a container that frequently request the container created prevously 
- deploy an autoscaler for kubernetes and let it scale-up and down 