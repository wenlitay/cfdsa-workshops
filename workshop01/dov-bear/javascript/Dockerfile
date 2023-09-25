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
ENV PORT=5000 INSTANCE_NAME="dov bear" INSTANCE_HASH="abc123"

ENTRYPOINT node main.js
