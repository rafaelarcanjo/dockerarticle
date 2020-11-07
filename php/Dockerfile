FROM php:7.2-apache
COPY "./php.ini" "$PHP_INI_DIR/php.ini"
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        ffmpeg \
        && docker-php-ext-configure gd \
        && docker-php-ext-install -j$(nproc) gd \
        && docker-php-ext-install mysqli \
        && a2enmod rewrite 
