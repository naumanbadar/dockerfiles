FROM java:8-jdk


#install activator
RUN cd /opt \
&& apt-get -y install unzip \
&& wget http://downloads.typesafe.com/typesafe-activator/1.3.10/typesafe-activator-1.3.10-minimal.zip \
&& unzip typesafe-activator-1.3.10-minimal.zip \
&& ln -s /opt/activator-1.3.10-minimal/bin/activator /usr/local/bin/activator \
&& rm -f /opt/typesafe-activator-1.3.10-minimal.zip \
&& apt-get remove --purge -y unzip \
&& apt-get clean \
&& cd

WORKDIR /project
