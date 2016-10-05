FROM ruby:2.3-alpine
MAINTAINER Christoph Petschnig <christoph.petschnig@sage.com>

RUN apk --upgrade --update --no-cache --virtual add \
                build-base \
                git \
                mysql-dev \
                openssh-client \
        \
        && rm -rf /var/cache/apk/* \
        \
        && gem install \
                byebug \
                eventmachine \
                ffi \
                hiredis \
                mysql2 \
                nokogiri \
                oj \
                puma \
                thin \
        \
        && gem sources --clear-all \
        \
        # remove static libs for smaller image size
        && rm /usr/lib/*.a
