#### Links

Alle Code-Beispiele findet ihr unter:

* https://github.com/Lhdang88/cloud_computing_ws

down:

#### Hello World in NodeJS

<span>
<img src="media/hello_world_female.jpg" width="50%" height="50%" class="fragment" data-fragment-index="1"/>
<img src="media/hello_world_male.jpg" width="40%" height="40%" class="fragment" data-fragment-index="2"/>
</span>

down:

#### Hello World in NodeJS

in your Shell / Terminal (Ubuntu: CTRL + Alt + T)
```bash
cd into-your-directory
git clone https://github.com/Lhdang88/cloud_computing_ws.git
cd cloud_computing_ws
git checkout hello_world
```

down:

#### Hello World in NodeJS

```javascript
//install dependencies
npm install
//start the application with
npm start
//stop the application with CTRL+C
```

down:

## What is Docker

<iframe width="560" height="315" src="https://www.youtube.com/embed/UFLCdmfGs7E" frameborder="0" allowfullscreen></iframe>

down:

#### Docker Demo

![ShowTime](media/showtime.gif)<!-- .element: class="fragment" data-fragment-index="1" -->

down:

#### Pull & Run someone's Docker Image

[https://hub.docker.com/_/mongo/](https://hub.docker.com/_/mongo/)

```bash
# pull and run mongo-db a NoSQL DB
docker run --name my-mongodb-name -p 27017:27017 -itd mongo
# confirm with
docker ps -a
# try to connect with a MongoDB Client
```

down:

#### Konzept: App-Containerisierung

![packaging](media/packaging.gif)

down:

#### Dockerize Your Application

In your app-root-directory, create a file named 'Dockerfile'
Dockerize your app: Put this content in your Dockerfile
```bash
# Base OS from Dockerhub
FROM alpine:latest
# update software repository and install nodejs
RUN apk add --update nodejs
# copy local data into image
ADD . /myApp/
# install packages
RUN cd /myApp && npm install
# set working directory
WORKDIR /myApp
# start command
CMD npm start
```

down:

#### Build & Run Your-Own Image

API docu: https://docs.docker.com/engine/reference/commandline/build/
```bash
cd into-your-app-directory
# build the docker image with docker build
# if you need help: execute 'docker [Command] help'
docker build -t your-image-name:your-tag-name .
#confirm with
docker images
# run the docker image with docker run
docker run --name your-container-name -p 80:3000 -itd your-image-name:your-tag-name
# confirm with
docker ps -a
```

down:

#### Push Image to a repository

```bash
# re-tag it, to reference my docker-hub repository
docker tag your-image:your-tag lhdang88/dhbw:hello_world
# push the image to my repository on 'Docker-Hub'
docker push lhdang88/dhbw:hello_world
```

down:

#### Bring-Your-Own-Container

<div style="background-color: white">
<img src="media/CaaS-Simple.svg" width="60%" height="60%" />
</div>

down:

#### Hands-On: Microsoft Azure + Kubernetes
Container-as-a-Service (CaaS)

![containers](media/containers.gif)

down:

#### Cloud Foundry

* "Bring-Your-Own-Code"-Prinzip: Container-Image wird durch ein "Buildpack"-script gebaut
* Container-Updates werden durch die Plattform automatisch durchgeführt, bspw. Security-Patching, Runtime-Updates (siehe Verantwortlichkeit PaaS)
* Plattform startet/pausiert/rebootet/terminiert Container eigenständig
* Container = "Cell"

down:

#### "Bring-Your-Own-Code"

<img src="media/PaaS-Simple.svg" width="60%" height="60%" />

down:

#### Hands-On Cloud Foundry

Ein bisschen PaaS-Magic!<!-- .element: class="fragment" data-fragment-index="0" -->

<img src="media/magic_dude.gif" width="50%" height="50%" class="fragment" data-fragment-index="1" />

down:

#### Push Your Own Cloud Foundry App

create "manifest.yaml" in your app-root-directory with this content:
```yaml
---
applications:
- name: dhbw-hello-world
  memory: 512M
  disk_quota: 512MB
  buildpack: https://github.com/cloudfoundry/nodejs-buildpack
  command: node index.js

```

down:

#### Push Your Own Cloud Foundry App

```bash
cd into-your-app
# log into cloud Foundry, with the provided credentials
cf login -a the-cloud-foundry-endpoint
# push your app
cf push -f manifest.yaml  
```
