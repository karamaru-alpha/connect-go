Connectを試す
==

cf. https://github.com/bufbuild/connect-go

```shell
go run main.go

curl --header "Content-Type: application/json" --data '{"name": "Jane"}' http://localhost:8080/greet.v1.GreetService/Greet

grpcurl -protoset <(buf build -o -) -plaintext -d '{"name": "Jane"}' localhost:8080 greet.v1.GreetService/Greet
```
