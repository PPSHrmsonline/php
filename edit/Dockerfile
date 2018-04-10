FROM debian:unstable-slim

LABEL maintainer="Eakkapat Pattarathamrong (overbid@gmail.com)"

RUN set -x \
        && apt-get update \
        && apt-get dist-upgrade -y \
        && apt-get install --no-install-recommends -y \
            ca-certificates \
            git \
            neovim \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

#COPY .bashrc /var/www/.bashrc
RUN set -x \
        && mkdir -p /var/www/.local \
        && cp /etc/skel/.bashrc /var/www/.bashrc \
        && chown -R www-data: /var/www

USER www-data
