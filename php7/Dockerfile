FROM php:7-alpine

RUN apk --no-cache add \
    libmcrypt-dev \
    libxml2-dev \
    openssl \
    libzip-dev \
    libxrender-dev \
    libxext-dev 

RUN docker-php-ext-install \
    pdo_mysql \
    soap \
    intl \
    zip

WORKDIR /app

ENTRYPOINT ["php", "artisan"]
CMD ["list"]