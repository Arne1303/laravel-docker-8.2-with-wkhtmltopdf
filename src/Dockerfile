FROM ghcr.io/lorisleiva/laravel-docker:8.2

# Installing curl
RUN apk update
RUN apk add --no-cache wkhtmltopdf

RUN ln -s /usr/bin/wkhtmltopdf /usr/local/bin/wkhtmltopdf;
RUN chmod +x /usr/local/bin/wkhtmltopdf;

# Clearing cache
RUN rm -rf /var/cache/apk/*
