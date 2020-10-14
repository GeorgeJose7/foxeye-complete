FROM openjdk:13
ADD ./target/customerlog.jar customerlog.jar
ADD application.properties application.properties
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "customerlog.jar" ]
