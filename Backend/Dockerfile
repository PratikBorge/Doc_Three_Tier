FROM centos:7
LABEL app="studentapp"
USER root
WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.99/bin/apache-tomcat-8.5.99.tar.gz .
RUN tar -xzvf apache-tomcat-8.5.99.tar.gz
WORKDIR /opt/apache-tomcat-8.5.99
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war webapps/student.war
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar lib/mysql-connector.jar
COPY context.xml conf/context.xml
RUN yum install java -y
EXPOSE 8080
CMD [ "bin/catalina.sh", "run" ]