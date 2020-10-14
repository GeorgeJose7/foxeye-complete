FROM openjdk:13
ADD ./target/api-gateway.jar api-gateway.jar
ADD application.properties application.properties
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "api-gateway.jar" ]