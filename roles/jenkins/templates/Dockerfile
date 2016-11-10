FROM jenkins:alpine
USER root

RUN echo "biblicando" > /tmp/test

RUN echo http://dl-6.alpinelinux.org/alpine/edge/community >> /etc/apk/repositories \
    && apk update \
    && apk add docker

RUN mkdir /data
VOLUME /data

USER jenkins

COPY custom.groovy /usr/share/jenkins/ref/init.groovy.d/custom.groovy
RUN /usr/local/bin/install-plugins.sh \
    job-dsl \
    nodejs \
    github \
    docker-custom-build-environment \
    build-pipeline-plugin \
    javadoc \
    async-http-client