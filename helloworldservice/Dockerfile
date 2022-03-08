# Build the application first using Maven
FROM maven:3.8-openjdk-11 as build
WORKDIR /ocp/deployment
COPY . .
RUN mvn install

# Inject the JAR file into a new container to keep the file small
FROM openjdk:8-jre-alpine
WORKDIR /ocp/deployment
COPY --from=build /target/helloworldservice.jar /ocp/deployment/helloworldservice.jar
EXPOSE 8080
ENTRYPOINT ["sh", "-c"]
CMD ["java -jar helloworldservice.jar"]
