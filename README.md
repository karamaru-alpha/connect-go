Connectを試す
==

cf. https://github.com/bufbuild/connect-go

```shell
go run main.go

curl --header "Content-Type: application/json" --data '{"name": "Jane"}' http://localhost:8080/greet.v1.GreetService/Greet

grpcurl -protoset <(buf build -o -) -plaintext -d '{"name": "Jane"}' localhost:8080 greet.v1.GreetService/Greet
```

<img width="1207" alt="スクリーンショット 2022-06-28 14 07 20" src="https://user-images.githubusercontent.com/38310693/176097322-2c103c11-d359-43d3-af8c-0572943c51dc.png">
