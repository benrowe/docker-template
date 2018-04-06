FROM php:7.1-fpm-alpine

RUN apk --no-cache add --virtual .build-deps $PHPIZE_DEPS \
    && apk --update add zlib-dev git \
    && docker-php-ext-install zip bcmath mbstring pdo pdo_mysql opcache \
    && pecl install redis xdebug \
    && docker-php-ext-enable redis \
    && docker-php-ext-enable xdebug \
    && docker-php-source delete \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer

