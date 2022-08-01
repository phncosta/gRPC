# Exemplo de implementação de gRPC - Prática Full Cycle 

1. Suba o container rodando:
```
docker-compose up -d
```

2. Acesse o container:
```
docker-compose exec app sh
```

3. Caso queira gerar novamente as stubs:
```
protoc --proto_path=proto/ proto/*.proto --plugin=$(go env GOPATH)/bin/protoc-gen-go-grpc --go-grpc_out=. --go_out=.
```

4. Execução do servidor (no container)
```
go run cmd/server/server.go
```

4. Execução do client (no container)
```
go run cmd/client/client.go
```

<i>Credits: </i> [Full Cycle Course](https://github.com/codeedu/fc2-grpc)