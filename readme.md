Basic Dockerfile: Containerize a Simple App

To containerise any app, we need either the packaged source code or just a source code. 
If not in compile , first generate the .jar and then write the docker file.

######## Simple-docker_file ########
====================================
1) Java web application
2) POM.xml
3) Install mvn 
4) Run mvn clean package
5) you will get the .jar 
6) Write the Docker file
7) Build and run image
8) see the running container



### MultistageDockerfile 
==================================

1) Write the Docker file
Stage 1 --> to get .jar from plain src code 
1) Java web application
2) POM.xml
3) Install mvn 
4) Run mvn clean package
5) you will get the .jar 

Stage 2 ---> 
6) jre- java run time
7) .jar run 
8) expose port

** Build the image **



### docker-compose-java-mysql
============================================

1) It is used to manage multiple services (conatiner)
2) To run the container we use pre-built available images in the file, it will run the container from it.
3) if image not available or need latest version app image, we can put the docker file at root directory where docker compose file is there and built image while running compose up.
<<used when have frequent code changes in app or dockerfile >>
4) put environment variable in env file to refer its valae at run time.
5) depends on says , make up service B only if service A is up and running.


### docker network bridge and host network
================================================
1) Pulled an image - nginx 
2) Pulled another image - alpine
3) created a network - my-bridge-network
4) run the containers using above metwork
5) login to alpine and try to ping nginx container.
6) ping should get reply
7) now change the network type to host
8) run another container call web2 using nginx and assign host network
9) now try to ping web2 , it will not get any reply from alpine as both are in different network.

