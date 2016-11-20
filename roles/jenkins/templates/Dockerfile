FROM jenkins:alpine
USER root

RUN echo "biblicando" > /tmp/test

RUN echo http://dl-6.alpinelinux.org/alpine/edge/community >> /etc/apk/repositories \
    && apk update \
    && apk add docker \
    && apk add openrc --no-cache

VOLUME /tmp

#USER jenkins

RUN /usr/local/bin/install-plugins.sh \
    job-dsl \
    nodejs \
    github \
    build-pipeline-plugin \
    javadoc \
    async-http-client \
    gradle \
    groovy \
    git \
    docker-commons