FROM php:7.0-zts
RUN apt-get update 
RUN apt-get install -y cron 
RUN pecl install pthreads
RUN docker-php-ext-install mysqli pdo pdo_mysql mbstring opcache
RUN docker-php-ext-enable pthreads
RUN touch /var/log/cron.log
CMD cron && tail -f /var/log/cron.log