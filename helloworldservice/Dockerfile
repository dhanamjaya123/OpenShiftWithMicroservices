FROM openjdk:11-slim as build

WORKDIR /app

COPY .  .

RUN mvn package && \
    mv target/helloworldservice-jar-with-dependencies.jar /run/helloworldservice.jar && \
    rm -rf /app/*


CMD java  -jar /run/helloworldservice.jar
