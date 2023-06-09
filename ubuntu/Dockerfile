#docker file ubuntu
====================
FROM ubuntu
RUN apt-get update -y
RUN apt-get install apache2 -y
COPY index.html /var/www/html/
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]

#dockerfile jquery-template
# ==============================
ARG TAG=latest
FROM ubuntu:${TAG}
RUN apt update \
   && apt install -y apache2 zip \
   && apt install -y apache2-utils \
   && apt clean
ADD https://www.free-css.com/assets/files/free-css-templates/download/page292/grandcoffee.zip /tmp/
RUN cd /tmp \
    && unzip /tmp/grandcoffee.zip \
    && cp -r /tmp/html/* /var/www/html/
# COPY grandcoffee.zip /tmp/
EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]

# =======================
# tomcat dockerfile:
# ======================
# FROM ubuntu:latest
# WORKDIR /opt/
# RUN apt-get update && apt-get install -y wget
# RUN apt install default-jdk -y
# RUN wget -P /opt/ https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.7/bin/apache-tomcat-10.1.7.tar.gz
# RUN tar -xvzf /opt/apache-tomcat-10.1.7.tar.gz 
# RUN mv /opt/apache-tomcat-10.1.7/ /opt/tomcat/ && chmod -R 755 /opt/tomcat/










































#docker file react js 
----------------------
# Fetching the latest node image on apline linux
FROM node:12

# Setting up the work directory
WORKDIR /react-app

# Installing dependencies
COPY ./package.json /react-app
RUN npm install

# Copying all the files in our project
COPY . .

# Expose the Port Number
EXPOSE 3000

# Starting our application
CMD npm start


container command :

docker exec -it imageid sh  


#--------------------------------------

# Dockerfile ubuntu tomcat 

FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-8-jdk wget
RUN mkdir /usr/local/tomcat
RUN curl -O https://dlcdn.apache.org/tomcat/tomcat-10/v10.0.27/bin/apache-tomcat-10.0.27.tar.gz
RUN tar -xvzf apache-tomcat-10.0.27.tar.gz
RUN mv apache-tomcat-10.0.27 tomcat 
EXPOSE 8080
CMD ["/opt/tomcat/bin/sh.startup.sh", "run"]


# RUN 
# RUN /usr/local/tomcat/
# EXPOSE 8080
# CMD /usr/local/tomcat/bin/catalina.sh run