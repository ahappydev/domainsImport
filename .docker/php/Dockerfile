FROM php:7.4-fpm

WORKDIR /var/www/php

COPY . ./

RUN apt-get update -y && apt-get install -y --no-install-recommends libmcrypt-dev openssl libzip-dev zip ntp whois

RUN docker-php-ext-install pdo_mysql sockets zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN composer install