# docker-tomcat

##### Getting Started

First of all, You need to install [docker](https://www.docker.com/) first. this dockerFile require official centos images

##### install base images

base images not in [docker official mirror image](store.docker.com),in this repo [docker-centos-6.8](www.github.com/betwowt/dokcer-Self-built-script/tree/master/docker-centos-6.8)

> docker pull betwowt/centos:6.8

##### build images

>  docker build github.com/betwowt/dokcer-Self-built-script/tree/master/docker-tomcat-9.0.4 -t betwowt/tomcat

##### run images

>  docker run -d -p 8080:8080 betwowt/tomcat

http://localhost:8080/