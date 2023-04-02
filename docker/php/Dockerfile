# List of PHP extensions needed to run Wordpress
# https://make.wordpress.org/hosting/handbook/server-environment/
ARG PHP_VERSION
ARG PHP_VARIANT

FROM php:$PHP_VERSION-$PHP_VARIANT

MAINTAINER Jared Howland <caddy-stack@jaredhowland.com>

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

ARG PHP_EXTENSIONS
RUN apk add nodejs npm && \
    chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions $PHP_EXTENSIONS
