FROM mhart/alpine-node:base-7

ENV npm_config_cache=/data/npm
ENV npm_config_cache_min=9999999999
EXPOSE {{application_port}}

# configure wget with ssl
RUN   apk update \
  &&   apk add tar \
  &&   apk add ca-certificates wget \
  &&   update-ca-certificates

VOLUME /data/npm
WORKDIR /src

CMD ["/bin/sh"]