FROM rnsloan/redis
MAINTAINER R Sloan "rnsloan1@gmail.com"
ENV REFRESHED_AT 2015-03-21

ENTRYPOINT [ "redis-server", "--logfile /var/log/redis/redis-replica.log", "--slaveof redis_primary 6379" ]

# docker run -d -h redis_replica1 --name redis_replica1 --link redis_primary:redis_primary rnsloan/redis_replica
