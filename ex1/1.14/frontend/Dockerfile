FROM node:16

WORKDIR /usr/src/app

COPY package*.json  ./

RUN npm install

COPY . .

ENV REACT_APP_BACKEND_URL=http://127.0.0.1:8080

RUN npm install -g serve
RUN npm run build

CMD ["npx", "serve", "-s", "-l", "5000", "build"]
EXPOSE 5000
