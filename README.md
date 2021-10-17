# go-api-examples
Examples of writing api apps with golang

## Simple Api

An Api project based on the example within the golang.org tutorials docs.

### Resources
* [golang.org](https://golang.org/): [Developing a RESTful API with Go and Gin](https://golang.org/doc/tutorial/web-service-gin)

### Useful commands
```bash
$ go mod init github.com/mkozigo/go-api-examples/simple-api

$ go get github.com/gin-gonic/gin
$ go mod tidy

$ go run main.go
$ curl GET http://localhost:8080/albums
$ curl POST http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
$ curl POST http://localhost:8080/albums \
    --header "Content-Type: application/json" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
$ curl GET http://localhost:8080/albums/2 --header "Content-Type: application/json

```