#
# MAINTAINER        Leejianhao <ljh@ipms.cn>
# DOCKER-VERSION    18.09.2
#
# Dockerizing maven: Dockerfile for building maven images
#
FROM       greencloud/jdk:1.8
MAINTAINER Leejianhao <ljh@ipms.cn>

ENV MAVEN_VERSION 3.6.0
ENV MAVEN_HOME /opt/maven

COPY apache-maven-${MAVEN_VERSION}-bin.tar.gz /opt/

RUN tar xzf /opt/apache-maven-${MAVEN_VERSION}-bin.tar.gz -C /opt && \
    mv /opt/apache-maven-${MAVEN_VERSION} /opt/maven  && \
    ln -s /opt/maven/bin/mvn /usr/bin/mvn

COPY settings.xml /opt/maven/conf/settings.xml

WORKDIR /usr/src/mavenworkdir

ENTRYPOINT mvn clean install -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true -Dmaven.test.skip=true
