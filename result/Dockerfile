FROM node:12-alpine
ENV NODE_VERSION 12.18.4
WORKDIR /app

COPY package*.json ./
COPY . /APP

RUN npm install


EXPOSE 80
CMD ["node", "server.js"]
