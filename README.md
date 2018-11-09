# Giga AI Docker
Our Docker Stack for both Development and Live Environment Purpose

## Things Inside
- Nginx
- PHP 7.2 (default), 7.1, 7.0, your choice.
- MySQL 5.7
- PHPMyAdmin without login by default
- `.env` file as the configuration file, helps you upstart with Laravel more convenience.
- Cron Schedule for Laravel by default, you can edit to fit your project.

## Running
- Install Docker CE.
- Run `docker-compose up -d` and let Docker do the rest