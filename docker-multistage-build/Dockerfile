FROM golang:1.12-alpine as builder
WORKDIR /go/src
COPY wiki.go .
RUN go build wiki.go

FROM alpine:3.9
LABEL maintainer="zhangming860612@sina.com"
COPY ./app/ /app/
COPY --from=builder /go/src/wiki /app/
RUN adduser -S -D -H -h /app appuser
RUN chown -R appuser /app
WORKDIR /app
EXPOSE 8080
CMD ./wiki

