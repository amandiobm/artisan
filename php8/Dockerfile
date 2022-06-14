FROM php:8-buster

RUN apt-get update \
    && apt-get install -y \
    libxml2-dev \
    libcurl3-dev \
    libzip-dev \
    libbz2-dev \
    libxrender-dev \
    libfontconfig \
    libxext-dev \
    openssl \
    && apt-get clean -y


RUN docker-php-ext-install \
    bz2 \
    pdo_mysql \
    soap \
    intl \
    zip

WORKDIR /app

ENTRYPOINT ["php", "artisan"]
CMD ["list"]