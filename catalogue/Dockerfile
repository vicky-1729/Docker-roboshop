FROM node:20
WORKDIR /opt/server
COPY *.js .
COPY package.json .
RUN npm install
ENV MONGO="true"\
    MONGO_URL="mongodb://<mongodb_docker_continer_name>:27017/catalogue"

CMD ["node","server.js"]


#we need to do helath check by logging into the container
#curl http://localhost:8080/helath
# in the output both ok means connection good
# while copying anything make sure all moving in good path are check