# FullCycle Arquitetura Hexagonal

## Golang

```bash
# Subindo o ambiente
docker-compose up -d
docker exec -it appproduct bash

# Iniciando um modulo
go mod init github.com/codeedu/go-hexagonal

# Execute test
go test ./...

# Mockgen
mockgen -destination=application/mocks/application.go -source=application/product.go application

# Sqlite
touch sqlite.db
sqlite3 sqlite.db
create table products(id string, name string, price float, status string);
.tables

# Cobra
cobra init --pkg-name=github.com/codeedu/go-hexagonal
cobra add cli
go run main.go cli
go run main.go cli --help
go run main.go cli -a=create -n=Product CLI -p=25.0
go run main.go cli -a=get --id=06ed731a-9b05-46d9-8dad-bc51bdd5fb80

cobra add http
go run main.go http
http://localhost:9000/product/06ed731a-9b05-46d9-8dad-bc51bdd5fb80
```
