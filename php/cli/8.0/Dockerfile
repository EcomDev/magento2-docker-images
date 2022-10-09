FROM php:8.0-cli-alpine

LABEL org.opencontainers.image.source=https://github.com/EcomDev/magento2-docker-images
LABEL org.opencontainers.image.description="PHP 8.0 CLI container for Magento 2"
LABEL org.opencontainers.image.licenses=MIT

COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer
COPY docker-php-* /usr/local/bin/
RUN chmod +x /usr/local/bin/*
RUN mkdir /tmp/composer
RUN docker-php-setup-dependencies