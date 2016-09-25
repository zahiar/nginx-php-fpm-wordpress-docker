# Dockerised setup for WordPress with New Relic support

## What is this?
This is a pre-configured Nginx, PHP-FPM (7) & MySQL (5.7) setup specifically geared towards WordPress Environments.
It also comes with built-in support for the New Relic PHP agent.

## Instructions
1. Checkout this repository
1. Add your source code into the `code` directory
1. Edit `nginx/site.conf` replacing MY_SITE.com with the domain of your site
1. Edit `php-fpm/newrelic.ini` adding in your own license key and application name
1. Edit `docker-compose.yml` to set your MySQL root password
1. Feel free to modify `db/mycnf` or `nginx/conf` or `php-fpm/php.ini` to add any custom configuration
1. Now run `docker-compose up` to build and start the containers
1. Once up and running, you should be able to access your site at `http://localhost`
