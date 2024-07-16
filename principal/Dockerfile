FROM golang:alpine AS builder

WORKDIR /usr/src/app

COPY fullcycle.go .

RUN go build -ldflags '-s -w' fullcycle.go


FROM scratch

WORKDIR /

COPY --from=builder /usr/src/app / 
 
CMD ["./fullcycle"]