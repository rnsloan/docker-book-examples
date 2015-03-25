FROM ubuntu:14.04
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-02-07

RUN apt-get update
RUN apt-get -y install redis-server redis-tools
EXPOSE 6379
ENTRYPOINT ["/usr/bin/redis-server"]

# docker run -d -p 6379 --name redis rnsloan/redis