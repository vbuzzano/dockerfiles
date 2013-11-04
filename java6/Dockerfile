# atc/java6 - Dockerfile

FROM ubuntu
MAINTAINER Vincent Buzzano <vincent.buzzano@gmail.com>

# Update and install necessary packages
RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get update && apt-get upgrade

# automatically accept oracle license
RUN echo oracle-java6-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections

# install oracle java 6
RUN apt-get install -y oracle-java6-installer
