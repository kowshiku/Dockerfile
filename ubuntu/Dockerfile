#docker file ubuntu
====================
FROM ubuntu
RUN apt-get update -y
RUN apt-get install apache2 -y
COPY index.html /var/www/html/
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]

#dockerfile jquery-template
==============================
FROM ubuntu
RUN apt-get update -y
RUN apt-get install  apache2 -y
RUN mkdir static
WORKDIR static
ADD https://www.free-css.com/assets/files/free-css-templates/download/page285/meyawo.zip .
WORKDIR meyawo
COPY * /var/www/html/
EXPOSE 80
CMD apachectl -D FOREGROUND


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



