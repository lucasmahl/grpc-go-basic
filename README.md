# grpc-go-basic

Código basado na [documentação](https://grpc.io/docs/languages/go/basics/).

## Antes de começar
- Instalar o [Go](https://go.dev/doc/install) instalado em seu computador.
- Instalar uma IDE, pode ser o [Visual Studio Code](https://code.visualstudio.com/).
- Instalar [Protocol Buffer Compiler](https://grpc.io/docs/protoc-installation/)

**Executar**
- go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
- go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
- export PATH="$PATH:$(go env GOPATH)/bin"

# Executando o projeto
No diretório raiz do projeto, Executar:       
```bash
$ make protoc
$ make init
```
Então execute o servidor na porta 50051:
```bash
$ go run server/server.go
```
Por fim, em um outro terminal, também na raiz do projeto, execute:
```bash
$ go run client/client.go
```

É para ser mostrado um log na tela, como este:
```bash
$ Getting feature for point (409146138, -746188906)
    name:"Berkshire Valley Management Area Trail, Jefferson, NJ, USA" location:<latitude:409146138 longitude:-746188906 >
    Getting feature for point (0, 0)
    location:<>
    Looking for features within lo:<latitude:400000000 longitude:-750000000 > hi:<latitude:420000000 longitude:-730000000 >
    name:"Patriots Path, Mendham, NJ 07945, USA" location:<latitude:407838351 longitude:-746143763 >
    ...
    name:"3 Hasta Way, Newton, NJ 07860, USA" location:<latitude:410248224 longitude:-747127767 >
    Traversing 56 points.
    Route summary: point_count:56 distance:497013163
    Got message First message at point(0, 1)
    Got message Second message at point(0, 2)
    Got message Third message at point(0, 3)
    Got message First message at point(0, 1)
    Got message Fourth message at point(0, 1)
    Got message Second message at point(0, 2)
    Got message Fifth message at point(0, 2)
    Got message Third message at point(0, 3)
    Got message Sixth message at point(0, 3)
```