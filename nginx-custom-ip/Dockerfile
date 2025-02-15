FROM ubuntu:latest
RUN apt update && apt install -y nginx && rm -rf /var/lib/apt/lists/*
RUN rm -rf /usr/share/nginx/html/*
COPY index.html /usr/share/nginx/html/index.html
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
EXPOSE 80
CMD ["/bin/bash", "-c", "/entrypoint.sh && nginx -g 'daemon off;'"]
