FROM php:7.4-fpm-alpine

# Install Dependencies
RUN apk update && \
    apk add --no-cache libpng-dev libjpeg-turbo-dev freetype-dev

# Install PHP Extensions
RUN docker-php-ext-configure gd --with-freetype --with-jpeg && \
    docker-php-ext-install -j$(nproc) gd && \
    docker-php-ext-install -j$(nproc) pdo_mysql && \
    docker-php-ext-install -j$(nproc) exif
