FROM php:8.2-rc-cli-alpine

LABEL org.opencontainers.image.source=https://github.com/EcomDev/magento2-docker-images
LABEL org.opencontainers.image.description="PHP 8.2 CLI container for Magento 2"
LABEL org.opencontainers.image.licenses=MIT

COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer
COPY docker-php-* /usr/local/bin/
RUN chmod +x /usr/local/bin/*
RUN docker-php-setup-dependencies

ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /tmp