FROM node:alpine

WORKDIR /app

COPY *.json ./
COPY *.js ./
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/users" \
    REDIS_URL="redis://redis:6379"
RUN npm install

CMD ["node", "server.js"]