FROM alpine:3.10

RUN apk add --update \
    python3=3.6.8-r2 \
    python3-dev=3.6.8-r2 \
    py-pip \
    build-base \
    openjdk8-jre \
    postgresql-libs \
    zip \
  && apk add --no-cache --virtual .build-deps gcc musl-dev postgresql-dev bash \
  && apk --purge del .build-deps \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*
