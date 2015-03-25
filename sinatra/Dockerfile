FROM ubuntu:14.04
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-02-07

RUN apt-get update
RUN apt-get -y install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /opt/webapp

EXPOSE 4567
CMD ["/opt/webapp/bin/webapp"]

# docker run -d -p 4567 --name webapp -v $PWD/webapp:/opt/webapp/ rnsloan/sinatra
# docker run -p 4567 --name webapp --link redis:db -t -i -v $PWD/webapp:/opt/webapp rnsloan/sinatra /bin/bash