FROM centos
MAINTAINER betwowt betwowt@163.com

RUN yum install -y java-1.8.0-openjdk
#RUN mkdir -p /opt/jdk/
RUN mkdir -p /opt/tomcat/
#这里会将 jdk1.8.0_121 里的所有文件放入jdk目录下（不包含 jdk1.8.0_121 目录）
#ADD jdk1.8.0_121 /opt/jdk/
ADD http://mirrors.ocf.berkeley.edu/apache/tomcat/tomcat-9/v9.0.4/bin/apache-tomcat-9.0.4.tar.gz /opt/tomcat/
WORKDIR /opt/tomcat
RUN tar -xzvf apache-tomcat-9.0.4.tar.gz
RUN rm apache-tomcat-9.0.4.tar.gz
ENV CATALINA_HOME /opt/tomcat/apache-tomcat-9.0.4

#ENV JAVA_HOME /opt/jdk
EXPOSE 8080
ENV PATH $CATALINA_HOME/bin:$PATH
# 9.0.4版本修改了启动参数
CMD ["sh","catalina.sh","run"]
