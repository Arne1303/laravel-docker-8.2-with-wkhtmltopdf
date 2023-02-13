FROM ghcr.io/lorisleiva/laravel-docker:8.2

# Installing wkhtmltopdf
RUN apk update

RUN apk add --no-cache \
    libgcc libstdc++ libx11 glib libxrender libxext libintl \
    freetype freetype-dev ttf-freefont libressl libressl-dev \
    fontconfig ttf-dejavu ttf-droid ttf-freefont ttf-liberation \
    openssl1.1-compat

COPY --from=madnight/alpine-wkhtmltopdf-builder:0.12.5-alpine3.10-606718795 \
    /bin/wkhtmltopdf /bin/wkhtmltopdf

RUN chmod +x /bin/wkhtmltopdf;

# Clearing cache
RUN rm -rf /var/cache/apk/*
