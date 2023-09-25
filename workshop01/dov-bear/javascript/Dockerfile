FROM node:20

# BUILD
# mkdir /app and cd /app
WORKDIR /app

COPY main.js .
COPY package-lock.json .
COPY package.json .

COPY public public
COPY views views

RUN npm ci

# RUNNING
ENV APP_PORT=3000

EXPOSE ${APP_PORT}

ENTRYPOINT node main.js
