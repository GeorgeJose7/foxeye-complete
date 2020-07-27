FROM openjdk:13
ADD customerlog.jar customerlog.jar
ADD application.properties application.properties
EXPOSE 8082
ENTRYPOINT [ "java", "-jar", "customerlog.jar" ]