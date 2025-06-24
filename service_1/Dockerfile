FROM golang:1.24-alpine

WORKDIR /app

# Copy the source code
COPY . .

# Build the Go application
RUN go build -o /app/main .

# Expose the port the app runs on
EXPOSE 8001

# Run the binary
CMD ["/app/main"]
