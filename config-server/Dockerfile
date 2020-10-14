FROM openjdk:13
ADD ./target/config-server.jar config-server.jar
ADD application.properties application.properties
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "config-server.jar" ]