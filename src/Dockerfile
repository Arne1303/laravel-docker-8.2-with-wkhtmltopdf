FROM ghcr.io/lorisleiva/laravel-docker:8.2

# Installing wkhtmltopdf
RUN apk update
RUN apk add  --no-cache --repository  http://dl-cdn.alpinelinux.org/alpine/v3.10/main/ wkhtmltopdf=0.12.5-r0

RUN ln -s /usr/bin/wkhtmltopdf /usr/local/bin/wkhtmltopdf;
RUN chmod +x /usr/local/bin/wkhtmltopdf;

# Clearing cache
RUN rm -rf /var/cache/apk/*
