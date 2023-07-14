# Beginning a Go app from scratch

- Create a folder and inside the folder run `go mod init {appName}`
- Install the dependencies/packages by running `go get`
- Create a OpenApi spec `yml` file
- Run `go install github.com/deepmap/oapi-codegen/cmd/oapi-codegen@latest` to install `oapi-codegen` package which installs the OpenApi spec code generator
- Create an OpenApi spec based `{appName}.yml` file
- Generate the types of this spec file by running `oapi-codegen -generate types -o openapi_types.gen.go -package main {appName}.yml`
- Generate the server file by running `oapi-codegen -generate server -o openapi_server.gen.go -package main {appName}.yml`