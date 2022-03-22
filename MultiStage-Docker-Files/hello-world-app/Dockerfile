# Start from latest golang parent image
FROM golang:latest
# Set the working directory
WORKDIR /myapp
# Copy source file from current directory to container
COPY helloworld.go .
# Build the application
RUN go mod init example.com/m/v2
RUN go build -o helloworld .
# Run the application
ENTRYPOINT ["./helloworld"]