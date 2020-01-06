ARG PHP_VERSION=7.4

FROM php:${PHP_VERSION}-fpm-alpine

RUN apk update && \
    apk add --no-cache $PHPIZE_DEPS

RUN pecl install xdebug

RUN docker-php-ext-enable xdebug && \
    docker-php-ext-install pdo_mysql

RUN cp $(find /usr/local/etc/php -name "php.ini-development") /usr/local/etc/php/php.ini

RUN find /usr/local/lib/php -name "xdebug.so" -exec echo 'zend_extension="{}"' >> /usr/local/etc/php/php.ini

ARG PHP_FPM_XDEBUG_INI=xdebug.ini

COPY ../${PHP_FPM_XDEBUG_INI} /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

CMD["php-fpm"]
