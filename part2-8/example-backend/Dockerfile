FROM golang:1.16-alpine

WORKDIR /go/src/app

COPY . .

RUN apk add build-base

RUN go build
RUN go test ./...

CMD ["./server"]
