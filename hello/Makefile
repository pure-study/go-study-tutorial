BINARY=hello

build:
	echo "Building for every OS and Platform"
	go build -o bin/${BINARY} hello.go
	GOOS=freebsd GOARCH=amd64 go build -o bin/${BINARY}-freebsd-amd64 hello.go
	GOOS=linux GOARCH=amd64 go build -o bin/${BINARY}-linux-amd64 hello.go
	GOOS=windows GOARCH=amd64 go build -o bin/${BINARY}-windows-amd64 hello.go
	GOOS=darwin GOARCH=amd64 go build -o bin/${BINARY}-darwin-amd64 hello.go

run: build
	echo "Run the default binary..."
	./bin/${BINARY}

clean:
	go clean
	rm -rf bin

all: clean build
