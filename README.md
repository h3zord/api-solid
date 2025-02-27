<h1 align="center">Boas-vindas ao repositório do API Solid!</h1>

<br/>

## Objetivo

A <strong>API Solid</strong> é uma aplicação RESTful projetada para realizar check-ins em academias, é possivel fazer login, buscar as academidas mais próximas e realizar o check-in.

## O que foi desenvolvido?

A <strong>API Solid</strong> é uma api para realizar check-ins em academias próximas, foi escrita com Node.js e Typescript e utiliza os princípios do SOLID.

O framework Fastify foi usado para gerenciar as rotas, tratar as requisições HTTP e definir middlewares. O JWT (JSON Web Token) foi utilizado para autenticar as requisições que necessitam de um token válido, que é gerado após o login. Além disso, a biblioteca zod foi aplicada para validar os dados que são enviados através do corpo e parâmetros das requisições. O banco de dados usado foi o postgresql em conjunto com o prisma ORM para a abstração das queries.

O projeto foi dividido em: repositórios, que armazenam função que fazem chamadas e manipulam o banco de dados; use-cases, que são descrições detalhadas de como um sistema deve se comportar ao interagir com um usuário ou outro sistema para atingir um objetivo específico, e são implementados como classes ou serviços que contêm a lógica de negócio pura, sem dependência de frameworks ou infraestrutura; e http: que são a parte dos controllers e a conexão com o mundo externo.

Foi desenvolvido também testes unitários para todos os casos de uso, utilizando a biblioteca Vitest e repositórios em memória para simular o comportamento de um banco de dados.

## Linguagens e ferramentas
- Node.js
- Typescript
- Fastify
- JWT
- Zod
- Day.js
- Bcrypt.js
- Vitest
- Docker
- PrismaORM
- PostgreSQL

## Instalação e execução com docker

### 1 - Clone o repositório:
```
git clone git@github.com:h3zord/api-solid.git
```

### 2 - Entre no repositório:
```
cd api-solid
```

### 3 - Instale as dependências:
Caso utilize o npm
```
npm install
```
Caso utilize o yarn
```
yarn install
```

### 4 - Inicie os containers:
```
docker compose up -d
```

### 5 - Inicie a API:
Caso utilize o npm
```
npm run dev
```
Caso utilize o yarn
```
yarn run dev
```

### 4 - Execute os testes unitários:
Caso utilize o npm
```
npm run test
```
Caso utilize o Yarn
```
yarn run test
```


<strong>O container vai executar o node na porta 3333 e o banco de dados na porta 5432.</strong>
<br/>
➜ http://localhost:3333/