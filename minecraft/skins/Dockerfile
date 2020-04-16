FROM php:apache
RUN rm /etc/apt/preferences.d/no-debian-php
RUN apt-get update && apt-get install -y php-gd php-curl php-mysql git 
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN git clone https://github.com/riflowth/SkinSystem.git
RUN mv SkinSystem/* /var/www/html/
RUN rm -r SkinSystem
RUN chown -R www-data:www-data /var/www/html/
