FROM maven:3.5-jdk-8-alpine as stage1

WORKDIR /code

COPY .  /code

RUN mvn package -D skipTests

CMD java -jar target/worker-jar-with-dependencies.jar

#Stage 2

FROM openjdk:8-jre-alpine

WORKDIR /code

COPY --from=stage1 target/worker-jar-with-dependencies.jar /code


