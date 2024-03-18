FROM centos:7
LABEL APP="studentapp"
LABEL engg="prat"
USER root
RUN yum install mariadb105-server
RUN mysql -u root -e "ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1234';"
RUN mysql -u root -p1234 -e "create database studentapp;"
RUN mysql -u root -p1234 -e "use studentapp;"
RUN mysql -u root -p1234 studentapp -e "CREATE TABLE if not exists students(student_id INT NOT NULL AUTO_INCREMENT, student_name VARCHAR(100) NOT NULL, student_addr VARCHAR(100) NOT NULL, student_age VARCHAR(3) NOT NULL, student_qual VARCHAR(20) NOT NULL, student_percent VARCHAR(10) NOT NULL, student_year_passed VARCHAR(10) NOT NULL, PRIMARY KEY (student_id));"
RUN service mysql restart
EXPOSE 3306
