FROM node:alpine

WORKDIR /app

COPY *.json ./
COPY *.js ./
ENV MONGO=true \
    MONGO_URL="mongodb://mongodb:27017/catalogue"

RUN npm install

CMD ["node", "server.js"]