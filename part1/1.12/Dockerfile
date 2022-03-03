FROM node:16

WORKDIR usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm install -g serve
RUN npm run build

CMD ["npx", "serve", "-s", "-l", "5000", "build"]

EXPOSE 5000

