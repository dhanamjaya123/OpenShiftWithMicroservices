#Start with a base image containing Java runtime
FROM openjdk:11-slim
VOLUME /tmp
ADD target/*.jar helloworldservice.jar
ENV JAVA_OPTS="
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /helloworldservice.jar" ]
