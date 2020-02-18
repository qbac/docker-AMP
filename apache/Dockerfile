ARG APACHE_VERSION=""
FROM httpd:${APACHE_VERSION:+${APACHE_VERSION}}

RUN apt-get update; \
    apt-get upgrade -y;

# Copy apache vhost file to proxy php requests to php-fpm container
COPY apache.conf /usr/local/apache2/conf/apache.conf
RUN echo "Include /usr/local/apache2/conf/apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf
