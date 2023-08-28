## Descrição

Repositório do back-end feito com Nest.js (Backend)

## Para Mac M1

Vide `docker-compose.yaml` no projeto para ativar a configuração do MongoDB corretamente para rodar o banco de dados.

## Google API Key

Gere uma API Key no painel do Google Console, é necessário ativar o serviço de `Google Maps API`.

## Rodar a aplicação

Execute os comandos:

```
docker-compose up
```

Em outro terminal rode o comando para entrar no container do Docker:
```bash
docker compose exec app bash
```

E configure as dependências iniciais (rode somente dentro do container do Docker):
```
npm install
npx prisma generate
```

Rode a aplicação (rode somente dentro do container do Docker):
```bash
npm run start:dev
```

Acessar http://localhost:3000/routes.

Existe um arquivo na raiz do projeto Nest.js, o `api.http` que você pode usar para testar a aplicação com o plugin do VSCode [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client). Quando enviar dados na requisição, o Nest.js consumirá a mensagem e mostrará no console.
