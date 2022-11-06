FROM ubuntu:18.04

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Europe/Moscow

RUN apt-get update  && \
      apt-get upgrade -y && \
      apt-get install -y curl apache2 php php-cli php-common openssl
COPY index.html /var/www/html/index.html
ENV contenido prueba
RUN echo "$contenido" > /var/www/html/prueba.html

CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]