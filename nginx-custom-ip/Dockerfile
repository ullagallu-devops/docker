FROM ubuntu:latest
RUN apt update && apt install -y nginx && rm -rf /var/lib/apt/lists/*
RUN rm -rf /var/www/html/*
COPY index.html /var/www/html/index.html
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
EXPOSE 80
CMD ["/bin/sh", "-c", "/entrypoint.sh && nginx -g 'daemon off;'"]

