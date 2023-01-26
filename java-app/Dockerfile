FROM schoolofdevops/maven:spring as stage1

WORKDIR /app

COPY .  /app

RUN mvn spring-javaformat:apply && \
    mvn package -DskipTests && \
    mv target/spring-petclinic-2.3.1.BUILD-SNAPSHOT.jar /run/petclinic.jar

EXPOSE 8080 

CMD java  -jar /run/petclinic.jar

RUN mvn clean install -Dmaven.test.skip=true

#Stage 2

FROM openjdk:20-slim-buster

WORKDIR /app

COPY --from=stage1 /run/petclinic.jar /app