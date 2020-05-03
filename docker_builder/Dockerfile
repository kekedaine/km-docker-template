# Builder image kekedaine/km-node:12-builder
FROM node:12-alpine

WORKDIR /app

RUN apk --no-cache add \
    g++ make python git \
    && yarn global add node-gyp \
    && rm -rf /var/cache/apk/*

ONBUILD ADD package.json /app/
ONBUILD RUN yarn --pure-lockfile