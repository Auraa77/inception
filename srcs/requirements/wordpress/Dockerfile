FROM debian:bookworm

RUN apt-get update && apt-get install -y \
    php-fpm \
    php-mysql \
    curl \
    && rm -rf /var/lib/apt/lists/*

CMD [sh]