FROM openjdk:13
ADD ./target/customer.jar customer.jar
ADD application.properties application.properties
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "customer.jar" ]
