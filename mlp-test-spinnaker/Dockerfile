FROM centos
MAINTAINER sjeevanantham@csod.com
RUN mkdir /opt/tomcat/
WORKDIR /opt/tomcat
RUN curl -O http://apachemirror.wuchna.com/tomcat/tomcat-9/v9.0.33/bin/apache-tomcat-9.0.33.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-9.0.33/* /opt/tomcat/.
RUN yum -y install java
RUN java -version
WORKDIR /opt/tomcat/webapps
COPY target/mlp-test-spinnaker.war .
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]