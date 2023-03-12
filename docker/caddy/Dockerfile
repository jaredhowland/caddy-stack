ARG CADDY_VERSION
ARG CADDY_VARIANT
ARG CADDY_MODULES

FROM caddy:$CADDY_VERSION-builder-alpine as builder

MAINTAINER Jared Howland<caddy-stack@jaredhowland.com>

RUN xcaddy build $CADDY_MODULES
FROM caddy:$CADDY_VERSION-$CADDY_VARIANT

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
