FROM php:7.1-fpm-alpine

RUN apk --update add zlib-dev \
    && docker-php-ext-install zip bcmath \
    && docker-php-source delete \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer