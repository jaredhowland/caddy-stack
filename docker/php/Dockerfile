# List of PHP extensions needed to run Wordpress
# https://make.wordpress.org/hosting/handbook/server-environment/
ARG PHP_VERSION

FROM php:$PHP_VERSION-fpm

MAINTAINER Jared Howland<caddy-stack@jaredhowland.com>

ARG PHP_EXTENSIONS
RUN install-php-extensions $PHP_EXTENSIONS
