FROM alpine:latest

LABEL org.opencontainers.image.title="tor" \
      org.opencontainers.image.description="A lightweight docker container with running tor" \
      org.opencontainers.image.authors="Ilya San <finetnew@gmail.com>" \
      org.opencontainers.image.source="https://github.com/QluxLab/Sherlock" \
      org.opencontainers.image.licenses="MIT"

RUN apk add --no-cache tor curl && \
    mkdir -p /var/lib/tor && \
    chown -R tor:tor /var/lib/tor && \
    chmod 700 /var/lib/tor

EXPOSE 9050 9080

USER tor

CMD ["tor", "-f", "/etc/tor/torrc"]