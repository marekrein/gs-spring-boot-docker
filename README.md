Initially based on: https://spring.io/guides/gs/spring-boot-docker/

Initial folder has docker-compose setup with custom properties file:

Check out Dockerfile and docker-compose.


To start:
cd initial
./gradlew build
(sudo) docker-compose up


docker-compose changes port to 5090

http://localhost:5090
http://localhost:5090/actuator


Complete folder has spring docker recommended setup.

To start:
cd complete
./gradlew build
(sudo) docker run -p 8080:8080 -t springio/gs-spring-boot-docker

http://localhost:8080/ won't work, to connect:

(sudo) docker ps to see container
(sudo) docker inspect --format '{{ .NetworkSettings.IPAddress }}' <CONTAINER ID>
Should connect on resulting ip:8080




To update image on dockerhub, use:
./gradlew build docker
