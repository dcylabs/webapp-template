FROM php:7.0-fpm
RUN docker-php-ext-install mysqli pdo pdo_mysql mbstring opcache
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
RUN echo "error_reporting = E_ALL" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "display_startup_errors = On" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "display_errors = On" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_enable=1" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_connect_back=1" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.idekey=\"PHPSTORM\"" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_port=9001" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "date.timezone=Europe/Paris" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "opcache.max_accelerated_files = 20000" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "realpath_cache_size=4096K" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "realpath_cache_ttl=600" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
CMD php-fpm