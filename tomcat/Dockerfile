FROM tomcat:9.0.14-jre8

USER root

ADD tomcat-users.xml /usr/local/tomcat/conf/

ADD context.xml /usr/local/tomcat/webapps/manager/META-INF/

COPY ./webapps webapps/

RUN rm -rf /usr/local/tomcat/webapps/ROOT 


RUN ln -sf /usr/share/zoneinfo/Asia/Bangkok /etc/localtime
RUN dpkg-reconfigure -f noninteractive tzdata

RUN date

RUN cat /etc/timezone

CMD ["catalina.sh", "run"]