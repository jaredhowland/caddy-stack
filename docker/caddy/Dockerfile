ARG CADDY_VERSION
FROM caddy:$CADDY_VERSION-builder-alpine as builder
MAINTAINER Jared Howland<caddy-stack@jaredhowland.com>

# https://stackoverflow.com/a/63166856
ARG CADDY_MODULES

RUN xcaddy build $CADDY_MODULES
FROM caddy:$CADDY_VERSION

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
