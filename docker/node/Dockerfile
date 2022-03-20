FROM node:16.14-alpine
RUN mkdir -p /var/www/nuxt
# timezone
ARG TZ
WORKDIR /var/www/nuxt
COPY ./nuxt/ /var/www/nuxt/

RUN apk update && \
    apk upgrade && \
    yarn install

EXPOSE 3000

ENTRYPOINT ["yarn", "dev"]