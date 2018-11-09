FROM php:7.1-fpm
COPY ../php/entrypoint.sh /etc/entrypoint.sh
COPY ../php/schedule /etc/cron.d/schedule
RUN chmod 0777 /etc/entrypoint.sh
RUN chmod 0644 /etc/cron.d/schedule
RUN apt -yqq update
RUN apt -yqq install libxml2-dev
RUN apt -yqq install cron
RUN crontab /etc/cron.d/schedule
RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install xml
ENTRYPOINT /etc/entrypoint.sh