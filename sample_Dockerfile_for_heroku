# Base image is alpine
FROM alpine:latest

WORKDIR /raw

RUN apk update \
    && apk upgrade \
    && apk add --update --no-cache python3 \
    && apk add --update --no-cache nodejs \
    && apk add --update --no-cache npm \
    && apk add --update --no-cache git \
    && npm install bower -g 

RUN git clone https://github.com/densitydesign/raw.git \
    && cd raw \
    && bower install \
    && mv * ../


CMD python3 -m http.server $PORT
