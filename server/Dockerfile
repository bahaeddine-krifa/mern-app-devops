FROM node:lts-alpine

RUN apk upgrade --no-cache zlib \
    && npm install -g npm@12.2.2

WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .

EXPOSE 9000

CMD [ "npm" , "start" ]