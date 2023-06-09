FROM centos:7
RUN yum -y update
RUN yum -y install httpd httpd-tools
ADD index.html /var/www/html/index.html
EXPOSE 80
CMD ["/usr/sbin/httpd","-D","FOREGROUND"]

#-----------------------------------------------


# #--tomcat docker file 
# FROM centos
# RUN  yum install java -y
# RUN  amazon-linux-extras install java-openjdk11 -y
# RUN  mkdir /usr/local/tomcat
# RUN wget http://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.16/bin/apache-tomcat-8.5.16.tar.gz -O /tmp/tomcat.tar.gz
# RUN cd /tmp && tar xvfz tomcat.tar.gz
# RUN cp -Rv /tmp/apache-tomcat-8.5.16/* /usr/local/tomcat/
# EXPOSE 8080
# CMD  /usr/local/tomcat/bin/catalina.sh run


# FROM centos

# RUN mkdir /opt/tomcat/

# WORKDIR /opt/tomcat
# RUN curl -O https://dlcdn.apache.org/tomcat/tomcat-10/v10.0.27/bin/apache-tomcat-10.0.27.tar.gz
# RUN tar -xvzf apache-tomcat-10.0.27.tar.gz
# RUN mv apache-tomcat-10.0.27 tomcat 
# RUN yum -y install java
# RUN java -version

# EXPOSE 8080

# CMD ["/opt/tomcat/bin/sh.startup.sh", "run"]
