FROM debian:bullseye-slim

RUN apt-get update 
RUN apt-get install -y --no-install-recommends apache2 
RUN apt-get install -y --no-install-recommends libapache2-mod-php
RUN apt-get install -y --no-install-recommends php 
RUN rm -rf /var/lib/apt/lists/*
RUN rm -rf /var/www/html/*

COPY ./html/ /var/www/html/

VOLUME [ "/var/www/html" ]

WORKDIR /var/www/html

EXPOSE 80

CMD ["apache2ctl", "-DFOREGROUND"]
