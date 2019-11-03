FROM php:7.3.6-fpm-alpine3.9
RUN apk add --no-cache openssl bash nodejs npm
RUN docker-php-ext-install pdo pdo_mysql bcmath 

# RUN rm -rf /var/www/html
# RUN ln -s public /var/www/html/app

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html

EXPOSE 9000
ENTRYPOINT ["php-fpm"]
