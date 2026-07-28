FROM debian:bookworm

RUN apt-get update && apt-get install -y \
    nginx \
    openssl \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /etc/nginx/sites-enabled \
    && ln -sf /etc/nginx/sites-available/default /etc/nginx/sites-enabled/default

COPY ./conf/nginx.conf /etc/nginx/nginx.conf

COPY ./conf/sites-available/default /etc/nginx/sites-available/default

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout /etc/ssl/private/nginx.key \
    -out /etc/ssl/certs/nginx.crt \
    -subj "/C=FR/L=Paris/O=42/OU=student/CN=merazafi.42.fr"

CMD ["nginx", "-g", "daemon off;"]