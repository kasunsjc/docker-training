# Start from latest golang parent image
FROM golang:latest AS builder 
# Set the working directory
WORKDIR /myapp
# Copy source file from current directory to container
COPY helloworld.go .
RUN go env -w GO111MODULE=off
# Build the application
RUN go build -o helloworld .
# Start from latest alpine parent image
FROM alpine:latest AS runtime
# Set the working directory
WORKDIR /myapp
# Copy helloworld app from current directory to container
COPY --from=builder /myapp/helloworld .
# Run the application
ENTRYPOINT ["./helloworld"]