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

```npm ci``` ou ```yarn```

Copie as variáveis de ambiente

```sh
cp .env.example .env
```

Execute o ambiente do cliente grpc
```sh
npm run start:dev
```

Caso queira, pode gerar o build od projeto também

Para gerar o build do projeto
```sh
npm run build
```

Para rodar o projeto em ambiente de produção
```sh
npm start
```


