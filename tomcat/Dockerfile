FROM tomcat:9.0.13-jre8

ADD tomcat-users.xml /usr/local/tomcat/conf/

ADD context.xml /usr/local/tomcat/webapps/manager/META-INF/

COPY ./webapps webapps/

RUN rm -rf /usr/local/tomcat/webapps/ROOT 

CMD ["catalina.sh", "run"]
