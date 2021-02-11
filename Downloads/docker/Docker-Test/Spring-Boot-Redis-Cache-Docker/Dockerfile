FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD target/dockerTest-0.0.1-SNAPSHOT.jar dockerTest.jar
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /dockerTest.jar" ]

# For Java 8, try this
# FROM openjdk:8-jdk-alpine

# For Java 11, try this
FROM adoptopenjdk/openjdk11:alpine-jre

# Refer to Maven build -> finalName
ARG JAR_FILE=target/dockerTest-0.0.1-SNAPSHOT.jar dockerTest.jar

# cd /opt/app
WORKDIR C:\Users\bezaw\Downloads\docker\Docker-Test\Spring-Boot-Redis-Cache-Docker

# cp target/dockerTest-0.0.1-SNAPSHOT.jar /opt/app/app.jar
COPY ${JAR_FILE} app.jar

# java -jar /opt/app/app.jar
ENTRYPOINT ["java","-jar","app.jar"]

## sudo docker run -p 8080:8083 -t docker-spring-boot:1.0
## sudo docker run -p 80:8083 -t docker-spring-boot:1.0
## sudo docker run -p 443:8443 -t docker-spring-boot:1.0