FROM php:8.1-apache-bookworm

# 1. Install dependencies AND configure GD with JPEG support
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libxml2-dev \
    libzip-dev \
    libonig-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd mbstring xml zip \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# 2. Enable Apache Rewrite
RUN a2enmod rewrite \
    && sed -i 's/AllowOverride None/AllowOverride All/g' /etc/apache2/apache2.conf

WORKDIR /var/www/html

CMD ["apache2-foreground"]
