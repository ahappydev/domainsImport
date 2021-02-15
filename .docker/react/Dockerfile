FROM node:14.1-alpine AS builder

WORKDIR /var/www/react
COPY . ./
RUN npm install

RUN npm run build