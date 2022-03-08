#Start with a base image containing Java runtime
FROM openjdk:11-slim
COPY ./target/helloworldservice-0.0.1-SNAPSHOT.jar helloworldservice-0.0.1-SNAPSHOT.jar
CMD ["java","-jar","helloworldservice-0.0.1-SNAPSHOT.jar"]
