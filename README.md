Connectを試す
==

cf. https://github.com/bufbuild/connect-go

```shell
go run main.go

curl --header "Content-Type: application/json" --data '{"name": "Jane"}' http://localhost:8080/greet.v1.GreetService/Greet

grpcurl -protoset <(buf build -o -) -plaintext -d '{"name": "Jane"}' localhost:8080 greet.v1.GreetService/Greet
```

<img width="1186" alt="スクリーンショット 2022-06-28 14 06 36" src="https://user-images.githubusercontent.com/38310693/176097235-3d15dfba-6700-4964-a095-ce7dcceecd15.png">
