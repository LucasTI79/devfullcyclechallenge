### Instruções para executar


Baixe os submódulos do projeto
```sh
git submodule update --init --recursive
```

Suba o ambiente
```sh
docker compose up -d
```

Abra o ambiente do servidor grpc
```sh
docker exec -it server bash
```

Instale as dependências do cliente dentro do ambiente
```sh
go mod tidy
```

Copie as variáveis de ambiente

```sh
cp .env.example .env
```

Execute o ambiente do servidor grpc
```sh
go run main.go grpc
```

Abra o ambiente do cliente grpc
```sh
docker exec -it client bash
```

Instale as dependências do cliente dentro do ambiente

```npm i``` ou ```yarn```

Execute o ambiente do cliente grpc
```sh
npm start:dev
```

Caso queira, pode gerar o build od projeto também

Execute o ambiente do cliente grpc
```sh
npm run build
```

E após isso, rodar o ambiente de produção

Execute o ambiente do cliente grpc
```sh
npm start
```


