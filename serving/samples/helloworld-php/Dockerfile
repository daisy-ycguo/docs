# Use the official PHP 7.2 image.
# https://hub.docker.com/_/php
FROM php:7.2.6-apache

# Copy local code to the container image.
COPY index.php /var/www/html/

# Use the PORT environment variable in Apache configuration files.
RUN sed -i 's/80/${PORT}/g' /etc/apache2/sites-available/000-default.conf /etc/apache2/ports.conf

# Configure and document the service HTTP port.
ENV PORT 8080
EXPOSE $PORT
