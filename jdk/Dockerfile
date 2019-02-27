
# MAINTAINER        Leejianhao <ljh@ipms.cn>
# DOCKER-VERSION    18.09.2
#
# Dockerizing jdk: Dockerfile for building jdk images
#
FROM       greencloud/centos:7
MAINTAINER Leejianhao <ljh@ipms.cn>

ENV JAVA_VERSION 1.8.0
ENV JAVA_HOME /usr/lib/jvm/java-${JAVA_VERSION}-openjdk
ENV PATH $JAVA_HOME/bin:$PATH

# Install jdk
RUN yum -y install java-${JAVA_VERSION}-openjdk java-${JAVA_VERSION}-openjdk-devel && \
    yum clean all
