FROM node:23

LABEL maintainer=zane

WORKDIR /app

COPY package*.json .
COPY main.js .

COPY public public
COPY views views

#Install dependensies
RUN npm ci

ENV APP_PORT=3000

EXPOSE ${APP_PORT}

ENTRYPOINT node main.js