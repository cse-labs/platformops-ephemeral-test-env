FROM openjdk:18-slim-buster as build
WORKDIR /workspace/app

COPY mvnw .
COPY .mvn .mvn
COPY src src
COPY pom.xml .
RUN ./mvnw clean package -DskipTests

FROM openjdk:18-jdk-alpine3.14
VOLUME /tmp
ARG DEPENDENCY=/workspace/app/target

COPY --from=build ${DEPENDENCY}/demo-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]