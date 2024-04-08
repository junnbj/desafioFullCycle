FROM golang:alpine as builder
WORKDIR /go/src/app
COPY . .
RUN go build -o app .

FROM scratch
COPY --from=builder /go/src/app/app /app
CMD ["/app"]
