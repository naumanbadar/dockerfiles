FROM ubuntu:14.04

#install java 8
RUN apt-get -y update && apt-get -y install software-properties-common \
 && add-apt-repository ppa:webupd8team/java \
 && apt-get -y update \
 && echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections \
 && apt-get -y install oracle-java8-installer

