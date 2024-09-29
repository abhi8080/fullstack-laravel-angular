FROM php:8.2-fpm

# Set working directory to /app
WORKDIR /usr/src/app

# Install dependencies
RUN apt-get update && apt-get install -y \
    libzip-dev zip unzip \
    && docker-php-ext-install zip \
    && docker-php-ext-install pdo_mysql

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Copy the entire application code
COPY ./backend ./

# Install composer dependencies
RUN composer install --no-dev --prefer-dist
