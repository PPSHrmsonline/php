FROM debian:unstable-slim


RUN set -x \
        && apt-get update \
        && apt-get dist-upgrade -y \
        && apt-get install --no-install-recommends -y \
            ca-certificates \
            git \
            vim \
            neovim \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

RUN set -x \
        && mkdir -p /var/www/.local \
        && cp /etc/skel/.bashrc /var/www/.bashrc \
        && sed -i 's/#force_color_prompt=yes/force_color_prompt=yes/g' /var/www/.bashrc \
        && chown -R www-data: /var/www

USER www-data
