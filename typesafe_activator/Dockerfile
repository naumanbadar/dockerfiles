FROM ubuntu:14.04

#install java 8
RUN apt-get -y update && apt-get -y install software-properties-common \
 && add-apt-repository ppa:webupd8team/java \
 && apt-get -y update \
 && echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections \
 && apt-get -y install oracle-java8-installer

ENV activatorVersion 1.3.5

#install activator
RUN cd /opt \
&& apt-get -y install unzip \
&& wget http://downloads.typesafe.com/typesafe-activator/${activatorVersion}/typesafe-activator-${activatorVersion}-minimal.zip \
&& unzip typesafe-activator-${activatorVersion}-minimal.zip \
&& ln -s /opt/activator-${activatorVersion}-minimal/activator /usr/local/bin/activator \
&& rm -f /opt/typesafe-activator-${activatorVersion}-minimal.zip \
&& apt-get remove --purge -y unzip \
&& apt-get clean \
&& cd

#EXPOSE 9000

#RUN activator new TestSP play-scala
# && cd TestSP && activator run

#CMD java -version

#VOLUME ["/TestSP"]

#CMD
