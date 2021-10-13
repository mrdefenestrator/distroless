FROM golang:latest as go
WORKDIR /app
COPY hello.go ./
RUN go build hello.go

FROM scratch
WORKDIR /app
COPY --from=go /app/hello ./
ENTRYPOINT ["/app/hello"]
