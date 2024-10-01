FROM php:7.4-fpm

# 必要なPHP拡張をインストール
RUN docker-php-ext-install pdo pdo_mysql

# Composerをインストール
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 作業ディレクトリを設定
WORKDIR /var/www

# Laravelの依存関係をインストール
COPY . /var/www
RUN composer install

# パーミッションの設定
RUN chown -R www-data:www-data /var/www