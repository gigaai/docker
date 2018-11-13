FROM php:fpm
COPY ./entrypoint.sh /etc/entrypoint.sh
COPY ./schedule /etc/cron.d/schedule
RUN chmod 0777 /etc/entrypoint.sh
RUN chmod 0644 /etc/cron.d/schedule
RUN apt-get -y update
RUN apt-get -y install libxml2-dev
RUN apt-get -y install cron
RUN crontab /etc/cron.d/schedule
RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install xml
ENTRYPOINT /etc/entrypoint.sh
