ARG CADDY_VERSION

FROM caddy:$CADDY_VERSION-builder AS builder

MAINTAINER Jared Howland <caddy-stack@jaredhowland.com>

ARG CADDY_VERSION
ARG CADDY_MODULES

RUN xcaddy build $CADDY_MODULES
FROM caddy:$CADDY_VERSION

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
