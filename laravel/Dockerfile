FROM bitnami/laravel:8.6.9-debian-10-r5

LABEL maintainer="Mark.Hsieh <qqzcmark@gmail.com>"

USER root
RUN apt-get update -y
RUN apt-get install -y git vim net-tools

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 3000

WORKDIR /app
USER bitnami
ENTRYPOINT [ "/app-entrypoint.sh" ]
CMD [ "php", "artisan", "serve", "--host=0.0.0.0", "--port=3000" ]
