FROM openjdk:13
ADD ./target/discovery-server.jar discovery-server.jar
ADD application.properties application.properties
EXPOSE 8761
ENTRYPOINT [ "java", "-jar", "discovery-server.jar" ]
