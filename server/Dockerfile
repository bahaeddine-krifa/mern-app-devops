FROM node:lts-alpine

RUN apk upgrade --no-cache zlib

WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .

EXPOSE 9000

CMD [ "npm" , "start" ]