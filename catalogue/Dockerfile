FROM node:20
WORKDIR /opt/server
COPY .*js .
COPY .*json .
ENV MONGO="true"\
    MONGO_URL="mongodb://mongodb:27017/catalogue"
CMD ["node","server.js"]