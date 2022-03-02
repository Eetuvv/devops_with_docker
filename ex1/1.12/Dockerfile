FROM node:16
WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install

COPY . .

RUN npm install -g serve
RUN serve -s -l 5000 build
RUN npm run build

CMD ["node", "server.js"]

USER node
EXPOSE 5000
