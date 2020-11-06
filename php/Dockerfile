FROM php:7.4-fpm
COPY ./php.ini "$PHP_INI_DIR/php.ini"
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && mysqli \
    && pdo_mysql

