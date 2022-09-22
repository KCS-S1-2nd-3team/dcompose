FROM maven:3.8.6-openjdk-11-slim as maven-stage
COPY ./repository /root/.m2/repository
RUN apt-get update && \
    apt-get install -y git
WORKDIR /sourcecode
ADD ./sourcecode .
#RUN git clone https://github.com/CptBluebear/DockerBackendSample.git ./
RUN mvn package -Dmaven.test.skip=true

FROM eclipse-temurin:11.0.16.1_1-jre-alpine as jdk-stage
COPY --from=maven-stage /sourcecode/target/DockerBackendSample-0.0.1-SNAPSHOT.jar /server/server.jar
EXPOSE 8081
ENTRYPOINT ["java", "-jar", "/server/server.jar"]

