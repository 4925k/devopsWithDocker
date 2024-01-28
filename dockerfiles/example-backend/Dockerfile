FROM golang:alpine as builder

WORKDIR /usr/src/app

COPY . .

RUN go build

FROM scratch

COPY --from=builder /usr/src/app/server .

CMD ["./server"]