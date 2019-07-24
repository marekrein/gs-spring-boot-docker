FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD /target/gs-spring-boot-docker-0.1.0.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar", "-Dspring.config.location=${CONFIG_LOCATION}", "/app.jar"]
EXPOSE 8080