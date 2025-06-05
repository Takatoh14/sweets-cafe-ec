# docker/php/Dockerfile
FROM php:8.2-fpm

# 必要な拡張機能をインストール
RUN apt-get update && apt-get install -y \
  zip unzip curl git libonig-dev libxml2-dev libzip-dev \
  && docker-php-ext-install pdo pdo_mysql zip

# Composer インストール
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 作業ディレクトリ
WORKDIR /var/www
