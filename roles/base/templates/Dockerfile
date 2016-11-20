FROM mhart/alpine-node:latest

ENV npm_config_cache={{npm_cache_volume_path}}
ENV npm_config_cache_min=9999999999

RUN adduser -D jenkins -u 10000

# configure wget with ssl
RUN   apk update \
  &&   apk add tar \
  &&   apk add git \
  &&   apk add ca-certificates wget \
  &&   update-ca-certificates

VOLUME {{npm_cache_volume_path}}
VOLUME /tmp
WORKDIR /src

CMD ["/bin/sh"]