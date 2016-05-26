FROM java:8

MAINTAINER Nauman Badar <naumanb@kth.se>

# this is required otherwise it will give the error 'E: The method driver /usr/lib/apt/methods/https could not be found.'
RUN apt-get update \
&& apt-get install -y apt-transport-https

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list \
&& apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823 \
&& apt-get update \
&& apt-get install sbt

RUN mkdir project

WORKDIR project

