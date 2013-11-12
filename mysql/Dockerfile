# ATC Mysql Server - Docker
FROM ubuntu

MAINTAINER Vincent Buzzano <vincent.buzzano@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get upgrade && apt-get autoremove && apt-get clean
RUN apt-get install -y mysql-server

EXPOSE 3306

CMD ["/usr/bin/mysqld_safe", "--bind-address=0.0.0.0"]



