FROM golang:1.25

WORKDIR /usr/src/app

# Copy go mod files first (for caching)
COPY go.mod go.sum ./
RUN go mod download

# Copy the rest of the source
COPY . .

# Build the binary (main.go is in this folder)
RUN go build -o app

EXPOSE 5001

CMD ["./app"]
