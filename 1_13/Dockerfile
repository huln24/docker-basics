FROM golang:1.16.15

ENV PORT=8080
ENV REQUEST_ORIGIN=https://example.com

EXPOSE $PORT

WORKDIR /usr/src/app

COPY go.mod go.sum ./
RUN go mod download

COPY . ./

RUN go build

CMD ["./server"]
