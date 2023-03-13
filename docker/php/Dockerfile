# List of PHP extensions needed to run Wordpress
# https://make.wordpress.org/hosting/handbook/server-environment/
ARG PHP_VERSION
ARG PHP_VARIANT

FROM php:$PHP_VERSION-$PHP_VARIANT

MAINTAINER Jared Howland <caddy-stack@jaredhowland.com>

ARG PHP_EXTENSIONS
RUN docker-php-ext-install $PHP_EXTENSIONS
