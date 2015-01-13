FROM ubuntu:14.04
MAINTAINER anarcher <anarcher@gmail.com>

RUN apt-get update
RUN apt-get -y install zip libsqlite3-dev wget

RUN \
    wget downloads.drone.io/master/drone.deb && \
    dpkg -i drone.deb

EXPOSE 80
ENTRYPOINT ["/usr/local/bin/droned"]
#CMD ["/usr/local/bin/droned"]
