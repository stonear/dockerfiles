FROM golang:alpine

RUN \
    apk update && \
    apk --no-cache add curl && \
    apk --no-cache add git && \
    apk --no-cache add make && \
    apk --no-cache add rsync && \
    rm -rf /var/cache/apk/*

RUN \
    go install golang.org/x/tools/cmd/goimports@latest && \
    go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest && \
    go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest && \
    go install github.com/swaggo/swag/cmd/swag@latest
