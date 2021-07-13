FROM openjdk:8-jdk

MAINTAINER ken-ichi chiba <kchiba@hgc.jp>

RUN apt-get -y update
RUN apt-get install -y wget 

RUN mkdir -p /tools

WORKDIR /tools

RUN wget https://faculty.washington.edu/browning/beagle/beagle.28Jun21.220.jar
RUN ln -s $( find /tools -name "beagle.*.jar" ) beagle.jar

ENV CLASSPATH /tools/beagle.jar:$CLASSPATH
ENV PATH /tools:$PATH

