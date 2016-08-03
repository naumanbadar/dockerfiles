FROM java:8-jdk

MAINTAINER Nauman Badar <naumanb@kth.se>

ENV activatorVersion 1.3.10

#install activator
RUN cd /opt \
&& apt-get -y install unzip \
&& wget http://downloads.typesafe.com/typesafe-activator/${activatorVersion}/typesafe-activator-${activatorVersion}-minimal.zip \
&& unzip typesafe-activator-${activatorVersion}-minimal.zip \
&& ln -s /opt/activator-${activatorVersion}-minimal/bin/activator /usr/local/bin/activator \
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
