FROM php:7.3-fpm
 
MAINTAINER Fabiano Costa <fabiano@tco.inf.br>

ARG DEBIAN_FRONTEND=noninteractive

# Additional tools
RUN apt-get update 

RUN apt-get install -y apt-utils libssl-dev

RUN apt-get install --no-install-recommends -y  \
    curl \
    openssl

# Common php-ext and requirements
RUN apt-get install -y --no-install-recommends libpq-dev libz-dev

RUN docker-php-ext-install pcntl \
 && docker-php-ext-install session \
 && docker-php-ext-install phar \
 && docker-php-ext-install iconv \
 && docker-php-ext-install pdo

# Intl
RUN apt-get install -y --no-install-recommends zlib1g-dev libicu-dev g++ \
 && docker-php-ext-configure intl \
 && docker-php-ext-install intl

# Clear package lists
RUN rm -rf /var/lib/apt/lists/*

CMD ["php-fpm"]

EXPOSE 9000
