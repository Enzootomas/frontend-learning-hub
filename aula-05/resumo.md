# Aula 05 - Criando APIs para o Front-end

## Objetivo da Aula

Nesta aula aprendemos os principais conceitos relacionados à criação e utilização de APIs no desenvolvimento Front-end.

Também vimos como criar uma API REST utilizando Node.js e Express.js, trabalhar com operações CRUD, armazenar dados em JSON e conectar um Front-end React com um Back-end.

---

## API

API significa **Application Programming Interface**.

Uma API permite que aplicações diferentes se comuniquem.

No desenvolvimento web, é comum o Front-end fazer requisições para uma API para buscar, cadastrar, atualizar ou remover informações.

---

## Métodos HTTP

Os principais métodos HTTP utilizados em APIs são:

### GET

Utilizado para buscar informações.

Exemplo:

```http
GET /api/notes
```

### POST

Utilizado para criar um novo registro no servidor.

Exemplo:

```http
POST /api/notes
```

### PUT / PATCH

Utilizados para atualizar informações existentes (`PUT` substitui o recurso; `PATCH` atualiza parcialmente).

Exemplo:

```http
PUT /api/notes/:id
```

### DELETE

Utilizado para remover um registro específico pelo identificador.

Exemplo:

```http
DELETE /api/notes/:id
```

---

## Express.js, JSON e Postman

- **Express.js:** framework minimalista para Node.js que simplifica a criação de rotas, middlewares e servidores HTTP.
- **Persistência em JSON (`data.json`):** utilização do módulo nativo `fs` para ler e gravar notas em formato JSON durante os estudos de CRUD.
- **CORS:** liberação controlada de requisições entre origens distintas (ex.: Front-end na Vercel consumindo Back-end no Render).
- **Postman:** ferramenta para testar endpoints HTTP, organizar coleções de requisições e documentar parâmetros e códigos de resposta.

---

[⬅️ Voltar ao README da Aula 05](./README.md) | [⬅️ Voltar ao índice principal](../README.md)
