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

## Simple Api No Framework

An api example that uses the standard library and no additional http framework

### Resources
* youtube: [Let's build a REST API in Go with zero dependencies!](https://www.youtube.com/watch?v=2v11Ym6Ct9Q)

### Useful commands
```bash
$ go mod init github.com/mkozigo/go-api-examples/simple-api-no-framework

$ curl localhost:8080/coasters | jq
$ curl -v localhost:8080/coasters | jq
$ curl -I localhost:8080/coasters
$ curl -X POST localhost:8080/coasters -H 'content-type:application/json' --data '{"name": "Taron", "height": 30, "inPark": "Phantasialand", "manufacturer": "Intamin"}'
$ curl -X POST localhost:8080/coasters -H 'content-type: application/text' --data '{"name": "Taron", "height": 30, "inPark": "Phantasialand", "manufacturer": "Intamin"}'
```