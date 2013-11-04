# Play 1.2.7 - Dockerfile
FROM atcfm/java6
MAINTAINER Vincent Buzzano <vincent.buzzano@gmail.com>

# Update and install necessary packages
RUN apt-get update && apt-get upgrade && apt-get install -y unzip less curl

# Download play 1.2.7 and install binary to /opt
RUN curl -o /tmp/play.zip http://downloads.typesafe.com/play/1.2.7/play-1.2.7.zip
RUN unzip /tmp/play.zip -d /opt
RUN mv /opt/play-1.2.7 /opt/play
RUN rm /tmp/play.zip
RUN ln -s /opt/play/play /usr/bin/play

# create play projects directory
RUN mkdir -p /app

EXPOSE 9000

CMD ["help"]
ENTRYPOINT ["/opt/play/play"]
