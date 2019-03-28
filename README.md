# docker-java

# Steps to use docker for java by applying maven plugin

## Prerequisites
* Git
* Maven
    See [here](https://github.com/HuangMarco/knowledge-hub/blob/dev/linux-operation/linux_installation_softwares_components.md)
* Docker
* Java

## Download the souce code
Use git to pull the source code, then in the root directory:
```sh
mvn clean install -Ddocker 
docker images
docker image rm demo --force
docker run -p 8090:8080 demo-docker 
docker ps --all
docker rm -f <container-id>
docker rm -f $(docker ps -a -q)
docker run -p 8999:8080 demo
```

## Inspect one container
```sh
docker container ls --all
docker inspect <container-id>
```

## Visit the application
```
 curl http://localhost:8999/api/all
```

# Reference Link
Initialize a spring boot java project
https://start.spring.io/

<br>
Use below article as guide:
https://stackabuse.com/dockerizing-a-spring-boot-application/
<br>
source code of the reference project: https://github.com/dhananjay12/learning-spring/blob/master/demo-docker/pom.xml

<br>
High level for docker:
https://stackabuse.com/docker-a-high-level-introduction/


<br>
fabric8io/docker-maven-plugin:
https://github.com/fabric8io/docker-maven-plugin
<br>
https://dmp.fabric8.io/#build-assembly

<br>
https://codefresh.io/howtos/using-docker-maven-maven-docker/

<br>
Another guide for docker for java:
http://containertutorials.com/docker-compose/spring-boot-app.html


<br>
About the project.build.directory:
https://stackoverflow.com/questions/13354531/maven-project-build-directory
C5271838


<br>
API level to interact with docker:
https://www.baeldung.com/docker-java-api
