FROM node:16

WORKDIR /usr/src/app

COPY reaktor-pre-assignment/package* ./

RUN npm install

COPY reaktor-pre-assignment . 

CMD ["npm", "start"]
