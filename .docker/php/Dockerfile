FROM php:fpm-alpine

# Fix debconf warnings upon build
ENV DEBIAN_FRONTEND=noninteractive \
    # Workaround missing openssl issue https://github.com/docker-library/php/issues/924
    PHP_OPENSSL=yes

# Install ca root certificates
ADD https://curl.haxx.se/ca/cacert.pem /etc/ssl/certs/ca-certificates.crt

# Disable not used extension
RUN sed -ri "s/^\s*extension=/;extension=/g" /usr/local/etc/php/conf.d/docker-php-ext-sodium.ini && \
    docker-php-ext-install mysqli
