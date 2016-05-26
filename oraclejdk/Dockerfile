FROM ubuntu:latest

ENV PATH $PATH:/usr/lib/jvm/oracle_jdk8/bin:/usr/lib/jvm/oracle_jdk8/db/bin:/usr/lib/jvm/oracle_jdk8/jre/bin

ADD installations /installations

RUN mkdir -p /usr/lib/jvm \
&& tar -xvf /installations/jdk-8u72-linux-x64.gz -C /usr/lib/jvm \
&& mv /usr/lib/jvm/jdk1.8* /usr/lib/jvm/oracle_jdk8

