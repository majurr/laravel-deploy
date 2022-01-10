FROM php:7.4-fpm
WORKDIR "/api"

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && sync && \
    install-php-extensions gd xdebug intl oci8 redis zip

RUN install-php-extensions @composer

EXPOSE 9000