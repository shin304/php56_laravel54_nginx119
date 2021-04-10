FROM php:5.6-fpm

# install xdebug
RUN pecl install xdebug-2.5.5 && docker-php-ext-enable xdebug

#pdoインストール
RUN docker-php-ext-install pdo_mysql

#composerインストール
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

#gitインストール
RUN apt-get update
RUN apt-get install -y git
# update php.ini
COPY php.ini /usr/local/etc/php/php.ini