# Base image
FROM php:7-fpm
RUN apt-get update

# Alter user permissions to allow writing to mounted volume
RUN usermod -u 1000 www-data
RUN groupmod -g 1000 www-data

# Install PHP extensions
RUN apt-get install -y --no-install-recommends libpng12-dev
RUN docker-php-ext-install mysqli pdo pdo_mysql gd

# Install NewRelic PHP Agent
RUN apt-get install -y --no-install-recommends wget
RUN wget -O - https://download.newrelic.com/548C16BF.gpg | apt-key add -
RUN sh -c 'echo "deb http://apt.newrelic.com/debian/ newrelic non-free"> /etc/apt/sources.list.d/newrelic.list'
RUN apt-get update

RUN apt-get install -y --no-install-recommends newrelic-php5
RUN newrelic-install install
