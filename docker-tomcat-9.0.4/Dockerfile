FROM betwowt/centos:6.8

RUN yum install -y java-1.8.0-openjdk
RUN mkdir -p /opt/tomcat/
ADD https://gitee.com/betwowt/dokcer-Self-built-script/raw/master/docker-tomcat-9.0.4/apache-tomcat-9.0.4.tar.gz /opt/tomcat/
WORKDIR /opt/tomcat
RUN tar -xzvf apache-tomcat-9.0.4.tar.gz
RUN rm apache-tomcat-9.0.4.tar.gz
ENV CATALINA_HOME /opt/tomcat/apache-tomcat-9.0.4

EXPOSE 8080
ENV PATH $CATALINA_HOME/bin:$PATH
# 9.0.4版本修改了启动参数
CMD ["sh","catalina.sh","run"]
