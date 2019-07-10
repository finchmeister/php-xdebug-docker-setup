FROM php:7.3-fpm
WORKDIR "/application"

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY xdebug.ini $PHP_INI_DIR/conf.d/xdebug.ini