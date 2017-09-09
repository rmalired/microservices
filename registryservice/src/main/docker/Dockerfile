FROM tomcat:8.5-alpine
VOLUME /tmp
COPY registryservice-1.0.war /usr/local/tomcat/webapps/app.war
RUN sh -c 'touch /usr/local/tomcat/webapps/app.war'
EXPOSE 9011
ENTRYPOINT [ "sh", "-c", "java $JAVA -Djava.security.egd=file:/dev/./urandom -jar /usr/local/tomcat/webapps/app.war" ]