ARG CADDY_VERSION
FROM caddy:CADDY_VERSION-builder-alpine as builder

# https://stackoverflow.com/a/63166856
ARG CADDY_MODULES
RUN xcaddy build \
    for MODULE in $CADDY_MODULES; do \
        echo "-- with $MODULE"; \
    done;

FROM caddy:CADDY_VERSION

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
