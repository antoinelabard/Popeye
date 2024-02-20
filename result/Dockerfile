FROM node:12-alpine
ENV NODE_ENV production
WORKDIR /usr/src/app

RUN npm install

COPY . .

EXPOSE 80
CMD node server.js
