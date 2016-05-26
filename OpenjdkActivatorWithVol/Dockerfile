FROM java:openjdk-8u66-jdk

MAINTAINER Nauman Badar <nauman.badar@ntsweden.se>

ENV activatorVersion 1.3.10

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

#create directory
RUN mkdir project

WORKDIR project
