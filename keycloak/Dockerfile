FROM jboss/keycloak
#ENV KEYCLOAK_USER admin
#ENV KEYCLOAK_PASSWORD password
ENV DB_VENDOR POSTGRES
ENV DB_ADDR keycloak-db
ENV DB_DATABASE keycloak
ENV DB_USER keycloak
ENV DB_SCHEMA public
ENV DB_PASSWORD password
#ENV PROXY_ADDRESS_FORWARDING: "true"
COPY realm-export.json /opt/jboss/keycloak/imports/realm-export.json 
ENV KEYCLOAK_IMPORT /opt/jboss/keycloak/imports/realm-export.json
ENV JDBC_PARAMS=useSSL=false
ENV DB_PORT 5432
EXPOSE 8080