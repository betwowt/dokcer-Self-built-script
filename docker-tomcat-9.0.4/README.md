# docker-tomcat

##### Getting Started

First of all, You need to install [docker](https://www.docker.com/) first. this dockerFile require official centos images

##### install centos images

> docker pull centos:6.8

Use [official image acceleration](https://www.docker-cn.com/registry-mirror) for Chinese developers

>docker pull registry.docker-cn.com/library/centos:6.8

##### build images

>  docker build docker-tomcat-9.0.4 -t tomcat:1.0

##### run images

>  docker run -d -p 8080:8080 tomcat:1.0

http://localhost:8080/