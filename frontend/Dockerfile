FROM golang:1.16

WORKDIR /usr/src/app
EXPOSE  8080

COPY go.mod ./

RUN go mod download && go mod verify

COPY . .
RUN go build -v -o /usr/local/bin/app ./...

CMD ["app"]