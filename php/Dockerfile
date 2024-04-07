FROM php:8.2.13RC1-fpm

RUN apt-get update


RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev && \
docker-php-ext-configure gd --with-freetype=/usr/include/ --with-jpeg=/usr/include/ && \
docker-php-ext-install gd


RUN docker-php-ext-install sockets

RUN apt-get install -y libbz2-dev
RUN docker-php-ext-install bz2
RUN docker-php-ext-install exif
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install bcmath


#RUN apt-get install icu-dev

RUN apt-get install -y libzip-dev
RUN apt-get install -y zip

#
RUN docker-php-ext-install zip
RUN docker-php-ext-install calendar
#
RUN apt-get install -y gettext


RUN docker-php-ext-configure gettext \
    && docker-php-ext-install gettext
#
RUN apt-get install -y libxml2-dev
RUN docker-php-ext-install soap
RUN docker-php-ext-install sysvmsg
RUN docker-php-ext-install sysvsem
RUN docker-php-ext-install sysvshm
#
RUN docker-php-ext-configure intl && docker-php-ext-install intl
#
RUN docker-php-ext-install opcache
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install pcntl

RUN apt-get install -y libxslt-dev

RUN docker-php-ext-install xsl
#
#
#
#
#
#RUN apt-get libmcrypt-dev
#
##RUN docker-php-ext-install mcrypt
#
#
#
##RUN curl -fsSLOJ https://pecl.php.net/get/mcrypt-1.0.6.tgz \
## && tar -xf mcrypt-1.0.6.tgz
##RUN cd mcrypt-1.0.6 \
## && phpize \
## && ./configure \
## && make \
## && make test \
## && cp modules/*.so $(pecl config-get ext_dir) \
## && cd .. \
## && rm -rf mcrypt-1.0.6.tgz mcrypt-1.0.6
##RUN echo extension="mcrypt.so" > /usr/local/etc/php/conf.d/php-ext-mcrypt.ini
#

# Install Composer
RUN	curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer
ENV PATH="/var/www/.composer/vendor/bin/:${PATH}"
RUN composer self-update 2.2.21

