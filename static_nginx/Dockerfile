FROM ubuntu:14.04
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-02-01
RUN apt-get update
RUN apt-install -y -q install nginx
RUN mkdir -p /var/www/html
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80

# sudo docker run -d -p 80 --name website -v $PWD/website:/var/www/html/website rnsloan/nginx nginx