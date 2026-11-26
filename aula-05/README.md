# Aula 05 — Criando APIs para o Front-end

Na Aula 05 aprofundamos a construção e a documentação de **APIs REST** voltadas ao consumo por aplicações Front-end, evoluindo o servidor **Express.js** para implementar um **CRUD completo** (*Create, Read, Update, Delete*) com persistência em arquivo **JSON** (`data.json`), integração com **React** e documentação de endpoints no **Postman**.

---

## 📌 Conteúdos Estudados

- Revisão de API, protocolo HTTP, endpoints, JSON, Backend e Web Services;
- Métodos HTTP aplicados a operações CRUD (`GET`, `POST`, `PUT`, `PATCH` e `DELETE`);
- Evolução de uma API estática em **Express.js** para uma API RESTful de notas;
- Leitura e escrita de dados em arquivo `data.json` com o módulo `fs` do Node.js;
- Uso de middlewares (`body-parser` / `express.json()` e **CORS**);
- Integração entre Front-end **React** e Back-end **Express.js**;
- Publicação do Back-end no **Render** e do Front-end na **Vercel**;
- Riscos de segurança, escalabilidade e boas práticas de arquitetura;
- Documentação e testes de APIs utilizando coleções no **Postman**.

---

## 🧠 Resumo Didático

### 1. Operações CRUD e Rotas REST

Em uma arquitetura RESTful, cada operação de manipulação de dados corresponde a um método HTTP combinado a um endpoint bem definido:

| Operação CRUD | Método HTTP | Endpoint | Finalidade |
|---|---|---|---|
| **Read (Listar)** | `GET` | `/api/notes` | Retorna todas as notas armazenadas |
| **Read (Detalhe)** | `GET` | `/api/notes/:id` | Retorna uma nota específica pelo seu `id` |
| **Create (Criar)** | `POST` | `/api/notes` | Cadastra uma nova nota com `id`, `titulo`, `texto` e data |
| **Update (Editar)** | `PUT` | `/api/notes/:id` | Atualiza `titulo` e `texto` de uma nota existente |
| **Delete (Excluir)** | `DELETE` | `/api/notes/:id` | Remove a nota correspondente ao `id` informado |

### 2. Servidor Express.js com Persistência em JSON

Para fins didáticos e prototipagem rápida, o servidor utiliza o módulo `fs` (*File System*) do Node.js para ler e gravar um array de objetos em `data.json`, enquanto o middleware de JSON interpreta o corpo (`req.body`) das requisições `POST` e `PUT`.

### 3. Documentação de APIs com Postman

Uma API profissional deve ser acompanhada de documentação técnica clara informando endpoints, métodos HTTP, parâmetros esperados, formatos de payload e códigos de status (`200 OK`, `204 No Content`, `404 Not Found`). O **Postman** permite organizar essas requisições em **coleções**, utilizar variáveis de ambiente (`{{baseUrl}}`), executar testes e compartilhar a documentação com a equipe.

### 4. Reflexões Arquiteturais Importantes

- **Segurança:** APIs abertas com `Access-Control-Allow-Origin: *` e sem validação ou autenticação ficam expostas a acessos indevidos; em produção deve-se restringir origens no CORS, validar entradas e autenticar usuários.
- **Limitações de arquivo JSON:** Funções síncronas (`fs.readFileSync` / `fs.writeFileSync`) bloqueiam o *Event Loop* e sofrem condições de corrida sob alto volume (ex.: 10.000 registros), além de perderem alterações em hospedagens efêmeras. Em produção utiliza-se banco de dados relacional ou NoSQL.
- **Modularização:** Concentrar rotas, regras e persistência em um único `server.js` dificulta a manutenção; recomenda-se separar em `routes/`, `controllers/` e `services/`.

---

## 💻 Exemplos Explicados

### Exemplo 1 — Estrutura CRUD em Express.js (`server.js`)

```javascript
const express = require("express");
const cors = require("cors");
const fs = require("fs");

const app = express();
const PORT = process.env.PORT || 3000;
const FILE = "data.json";

app.use(cors());
app.use(express.json());

function readNotes() {
  try {
    return JSON.parse(fs.readFileSync(FILE, "utf-8"));
  } catch {
    return [];
  }
}

function saveNotes(notes) {
  fs.writeFileSync(FILE, JSON.stringify(notes, null, 2));
}

app.get("/api/notes", (req, res) => {
  res.json(readNotes());
});

app.post("/api/notes", (req, res) => {
  const notes = readNotes();
  const novaNota = {
    id: Date.now().toString(),
    titulo: req.body.titulo,
    texto: req.body.texto,
    criadoEm: new Date().toISOString(),
  };
  notes.push(novaNota);
  saveNotes(notes);
  res.json(novaNota);
});
```

### Exemplo 2 — Formato de Armazenamento (`data.json`)

```json
[
  {
    "id": "1",
    "titulo": "Lembretes",
    "texto": "Comprar leite e pão",
    "criadoEm": "2026-04-28T10:00:00Z"
  }
]
```

---

## 🛠️ Atividades Solicitadas na Aula

1. **Atividade 01 — Atualização do Repositório da Disciplina:** Atualizar o repositório central de estudos com os arquivos e alterações realizadas e enviar o link pelo formulário acadêmico indicado pelo professor.
2. **Atividade 02 — Aplicação CRUD de Notas (Express + React) e Coleção Postman:**
   - Desenvolver a API REST de notas em **Express.js** com armazenamento em `data.json` e prepará-la para publicação no **Render**;
   - Desenvolver a aplicação Front-end em **React** consumindo todas as operações CRUD (`GET`, `POST`, `PUT`, `DELETE`);
   - Criar uma **coleção no Postman** documentando as operações CRUD, parâmetros e códigos de resposta.

---

## 🔗 Materiais, Referências e Projetos Relacionados

- 📄 **Material oficial da aula (PDF):** [Aula 05 - Criando APIs para o Front-end.pdf](./Aula%2005%20-%20Criando%20APIs%20para%20o%20Front-end.pdf)
- 📝 **Resumo complementar preservado:** [resumo.md](./resumo.md)
- 💻 **Projeto prático desenvolvido (Fullstack React + Express + Coleção Postman):** [🔗 Repositório](https://github.com/Enzootomas/notes-crud-fullstack) | [🌐 Ver online](https://notes-crud-fullstack.vercel.app)
- 📚 **Referências oficiais do professor:**
  - [Exemplo Back-end do Professor](https://github.com/deivisontakatu/exemplo-api-backend)
  - [Exemplo Front-end do Professor](https://github.com/deivisontakatu/exemplo-api-frontend)
  - [Aplicação modelo publicada (Notas App React)](https://notas-app-react.vercel.app/)

---

[⬅️ Voltar ao índice principal](../README.md)
