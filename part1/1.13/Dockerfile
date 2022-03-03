FROM golang:1.16-alpine

WORKDIR /app

ENV PORT=8080

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY . .

RUN go build
EXPOSE 8080

CMD ["./server"]
