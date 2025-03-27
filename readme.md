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



###### MultistageDockerfile #########
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



###
============================================