FROM python:3.11-alpine

WORKDIR /app

# Install build dependencies required for uwsgi
RUN apk add --no-cache \
    gcc \
    musl-dev \
    linux-headers \
    python3-dev \
    build-base

COPY requirements.txt /app/

RUN pip3 install --no-cache-dir -r requirements.txt

COPY payment.ini /app/
COPY payment.py /app/
COPY rabbitmq.py /app/

ENV CART_HOST="cart" \
    CART_PORT="8080" \
    USER_HOST="user" \
    USER_PORT="8080" \
    AMQP_HOST="rabbitmq" \
    AMQP_USER="roboshop" \
    AMQP_PASS="roboshop123"

CMD ["uwsgi", "--ini", "payment.ini"]