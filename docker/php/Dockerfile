FROM php:8.0-fpm

COPY php.ini /usr/local/etc/php/

RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libzip-dev \
    vim \
  && docker-php-ext-install zip pdo_mysql opcache


WORKDIR /var/www/html


COPY --from=composer /usr/bin/composer /usr/bin/composer
