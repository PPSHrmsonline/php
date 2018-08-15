FROM tomcat:8.5-jre8-slim

ARG UID=500
ARG GID=500

RUN groupmod -g $UID www-data \
        && usermod -u $GID www-data \
        && chown -R www-data: /usr/local/tomcat
