FROM node:18.13.0-alpine

USER root
WORKDIR /workspace/front

ARG NODE_MODULES="tslint-to-eslint-config typescript vue-cli"

RUN apk add git
RUN npm install -g npm@latest
RUN umask 0002 && npm install -g ${NODE_MODULES} \
    && npm cache clean --force > /dev/null 2>&1