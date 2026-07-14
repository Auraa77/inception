FROM debian:bookworm

RUN apt-get update && apt-get install -y \
    nginx \
    openssl \
    && rm -rf /var/lib/apt/lists/*

# RUN openssl req -x509 -nodes -days365 -newkey res:2048 -keyout /etc/ssl/private/nginx.key -out /etc/ssl/certs/nginx.crt -subj "/C=FR/L=Paris/O=42/OU=student/CN=merazafi.42.fr"

