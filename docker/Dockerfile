FROM php:7.3.11-apache

LABEL maintainer="Proshanta Barman <proshanta@brainstation-23.com>"

ARG TIMEZONE="Asia/Dhaka"

RUN echo "${TIMEZONE}" > /etc/timezone \
    && rm /etc/localtime \
    && dpkg-reconfigure -f noninteractive tzdata

WORKDIR /var/www/html

# Copy Code Files
COPY --chown=www-data:www-data ./src/ .

EXPOSE 80

CMD ["apache2-foreground"]

