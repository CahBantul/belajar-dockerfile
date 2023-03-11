FROM golang:1.18-alpine

RUN mkdir /app

RUN addgroup -S nzmgroup
RUN adduser -S -D -h /app nzmuser nzmgroup
RUN chown -R nzmuser:nzmgroup /app

USER nzmuser

COPY main.go /app

EXPOSE 8080
CMD go run /app/main.go