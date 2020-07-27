FROM openjdk:13
ADD customer.jar customer.jar
ADD application.properties application.properties
EXPOSE 8081
ENTRYPOINT [ "java", "-jar", "customer.jar" ]