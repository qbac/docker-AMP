ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm

RUN apt-get update; \
    apt-get upgrade -y;

# RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
COPY upload-file.ini /usr/local/etc/php/conf.d/upload-file.ini
# COPY php.ini-production /usr/local/etc/php/php.ini
# RUN echo "upload_max_filesize = 512M" >> /usr/local/etc/php/conf.d/docker-php-max-file.ini;
# RUN echo "post_max_size = 512M" >> /usr/local/etc/php/conf.d/docker-php-max-post.ini;
RUN docker-php-ext-install mysqli
