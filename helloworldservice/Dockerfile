#Start with a base image containing Java runtime
FROM openjdk:11-slim

ARG JAR_FILE=target/helloworldservice.jar
ARG JAR_LIB_FILE=target/lib/

# cd /usr/local/runme
WORKDIR /usr/local/runme

# copy target/find-links.jar /usr/local/runme/helloworldservice.jar
COPY ${JAR_FILE} helloworldservice.jar

# copy project dependencies
# cp -rf target/lib/  /usr/local/runme/lib
ADD ${JAR_LIB_FILE} lib/

# java -jar /usr/local/runme/app.jar
ENTRYPOINT ["java","-jar","helloworldservice.jar"]
