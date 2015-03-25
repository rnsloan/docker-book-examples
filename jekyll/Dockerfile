FROM ubuntu:14.04
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-02-26

RUN apt-get -yqq --fix-missing update
RUN apt-get -yqq install ruby ruby-dev make nodejs
RUN gem install --no-rdoc --no-ri jekyll

VOLUME ["/data/","/var/www/html"]
WORKDIR /data

ENTRYPOINT ["jekyll", "build", "--destination=/var/www/html"]
