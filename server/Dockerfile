FROM golang:1.22.1-alpine AS builder

WORKDIR /app

COPY go.mod .

COPY . .

RUN go build -o /server

FROM alpine

COPY --from=builder /server /server

CMD ["/server"]
