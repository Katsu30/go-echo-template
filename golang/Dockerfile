FROM golang:1.19.2-alpine

ENV GO111MODULE on

RUN apk update && \
    apk --no-cache add git && \
    apk add bash

WORKDIR /go/src/app

RUN go mod init app

RUN go mod tidy && \
    go install github.com/cosmtrek/air@v1.40.4

CMD ["air", "-c", ".air.toml"]