FROM php:7.3-fpm
WORKDIR "/application"

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

RUN echo "xdebug.remote_enable=on" >> $PHP_INI_DIR/conf.d/99-overrides.ini \
    && echo "xdebug.remote_autostart=off" >> $PHP_INI_DIR/conf.d/99-overrides.ini \
    && echo "xdebug.remote_host=host.docker.internal" >> $PHP_INI_DIR/conf.d/99-overrides.ini

