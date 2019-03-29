FROM node:10.15.3

RUN mkdir -p /usr/src/sportsstorejp

COPY dist/SportsStoreJP /usr/src/sportsstore/dist/SportsStoreJP


COPY authMiddleware.js /usr/src/sportsstorejp/
COPY serverdata.json /usr/src/sportsstorejp/
COPY server.js /usr/src/sportsstorejp/server.js
COPY deploy-package.json /usr/src/sportsstorejp/package.json

WORKDIR /usr/src/sportsstorejp

RUN npm install

EXPOSE 8088

CMD ["node", "server.js"]