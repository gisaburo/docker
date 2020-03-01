## Setup Docker Enviroment
- install docker
    - [Docker Engine overview](https://docs.docker.com/install/)
- install docker compose
    - [Install Docker Compose](https://docs.docker.com/compose/install/)
## Setup Podman Enviroment
- install podman
  ```
  $ sudo dnf install -y podman
  ```
- install podman-compose
  ```
  $ sudo dnf install -y podman-compose
  ```
## Create node application
```
$ mkdir <work dir>
$ npm init -y
$ npm i express
$ npm i typescript @types/express
$ ./node_modules/.bin/tsc --init
$ mkdir dist
$ npm run tsc
```
## Create dockerfile & docker-compose
```
$ touch dockerfile
$ touch docker-compose.yml
```
## Run application on podman
```
$ git clone https://github.com/gisaburo/SOA.git
$ cd SOA/iac/docker/nodejs
$ podman-compose up
```
## Stop application on podman
```
$ podman pod ls
$ podman pod stop nodejs
```
## Delete pod and container on podman
```
$ podman pod rm nodejs --force
```
