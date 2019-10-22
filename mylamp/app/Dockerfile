FROM php:7.2-apache-stretch
RUN apt-get update \
    && apt-get install -y vim cron libpng-dev \
    && docker-php-ext-install opcache mbstring zip mysqli pdo_mysql gd \
    && apt-get clean \
    && mkdir /var/log/php && chmod 777 /var/log/php \
    && a2enmod rewrite
COPY ./config/default.conf /etc/apache2/sites-available/000-default.conf
COPY ./config/php.ini /usr/local/etc/php/
COPY ./config/phpinfo.php /var/www/html/
ADD ./config/bashrc.txt /root/.bashrc