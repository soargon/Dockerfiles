FROM ubuntu

MAINTAINER soargon <soargon@gmail.com>

RUN apt-get update && apt-get -y install wget --no-install-recommends && rm -rf /var/lib/apt/lists/*\
	&& wget -P /tmp/java --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/7u67-b01/jdk-7u67-linux-x64.tar.gz \
	&& apt-get purge -y --auto-remove wget \
	&& mkdir /usr/local/jdk \
	&& tar -zxf /tmp/java/jdk-7u67-linux-x64.tar.gz -C /usr/local/jdk \
	&& rm -rf /tmp/java

ENV JAVA_HOME /usr/local/jdk/jdk1.7.0_67

ENV PATH $JAVA_HOME/bin:$PATH
