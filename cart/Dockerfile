FROM node:18.19.1-alpine3.19
EXPOSE 8080
WORKDIR /opt/server
COPY package.json .
COPY server.js .
RUN npm install
CMD ["server.js"]
ENTRYPOINT [ "node" ]