FROM debian:unstable-slim

LABEL maintainer="Eakkapat Pattarathamrong (overbid@gmail.com)"

RUN set -x \
        && apt-get update \
        && apt-get dist-upgrade -y \
        && apt-get install --no-install-recommends -y \
            git \
            neovim \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

RUN set -x \
        && mkdir -p /var/www/.local \
        && chown -R www-data /var/www/.local

USER www-data
