FROM ubuntu:14.04
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-03-21

RUN apt-get -yqq update
RUN apt-get -yqq install nodejs npm
RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN mkdir -p /var/log/nodeapp

ADD nodeapp /opt/nodeapp/

WORKDIR /opt/nodeapp

RUN npm install

VOLUME ["/var/log/nodeapp"]

EXPOSE 3000

ENTRYPOINT ["nodejs", "server.js"]

# docker run -d --name nodeapp -p 3000:3000 --link redis_primary:redis_primary rnsloan/nodejs
