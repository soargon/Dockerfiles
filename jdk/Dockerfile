FROM ubuntu

MAINTAINER soargon <soargon@gmail.com>

ENV JDK_MAJOR 7
ENV JDK_MINOR 67

RUN apt-get update && apt-get -y install wget --no-install-recommends && rm -rf /var/lib/apt/lists/*\
	&& wget -P /tmp/java --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/"$JDK_MAJOR"u"$JDK_MINOR"-b01/jdk-"$JDK_MAJOR"u"$JDK_MINOR"-linux-x64.tar.gz \
	&& apt-get purge -y --auto-remove wget \
	&& mkdir /usr/local/jdk \
	&& tar -zxf /tmp/java/jdk-"$JDK_MAJOR"u"$JDK_MINOR"-linux-x64.tar.gz -C /usr/local/jdk \
	&& rm -rf /tmp/java

ENV JAVA_HOME /usr/local/jdk/jdk1.$JDK_MAJOR.0_$JDK_MINOR

ENV PATH $JAVA_HOME/bin:$PATH
