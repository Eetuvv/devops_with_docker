FROM golang:1.16-alpine

WORKDIR /app

ENV REQUEST_ORIGIN=http://localhost:5000
ENV PORT=8080
ENV REDIS_HOST=redis

COPY go.mod ./

COPY go.sum ./
RUN go mod download

COPY . .

RUN go build

CMD ["./server"]

EXPOSE 8080
