#
# MAINTAINER        Leejianhao <ljh@ipms.cn>
# DOCKER-VERSION    18.09.2
#
# Dockerizing TOMCAT: Dockerfile for building TOMCAT images
#
FROM       greencloud/jdk:1.8
MAINTAINER Leejianhao <ljh@ipms.cn>

ENV CATALINA_HOME /tomcat
ENV APP_DIR ${CATALINA_HOME}/webapps/

COPY apache-tomcat-8.5.38.tar.gz apache-tomcat-8.5.38.tar.gz

RUN tar zxf apache-tomcat-*.tar.gz && \
    rm apache-tomcat-*.tar.gz && \
    mv apache-tomcat* tomcat

ADD scripts /scripts

EXPOSE 8080 8443

ENTRYPOINT ["/scripts/run"]

ONBUILD ADD . ${APP_DIR}
