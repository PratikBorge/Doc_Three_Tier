FROM centos:7
LABEL app="studentapp"

WORKDIR /opt/
ADD https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.99/bin/apache-tomcat-8.5.99.tar.gz
RUN tar -xzvf apache-tomcat-8.5.99.tar.gz
WORKDIR /opt/apache-tomcat-8.5.99
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war webapps/
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar lib/
COPY 