# Aula 06 — Projetos Front-End

Na Aula 06 foram estudados os fundamentos de **planejamento e gestão de projetos aplicados ao desenvolvimento Front-end**, abordando como transformar ideias em requisitos claros, estruturar e priorizar um backlog, estimar tarefas, aplicar o framework ágil **Scrum** e estabelecer critérios objetivos de conclusão (*Definition of Done*).

---

## 📌 Conteúdos Estudados

- Por que gerenciar um projeto Front-end?
- Gestão de Projetos Front-end (pessoas, tarefas, tecnologias e prazos);
- Gestão de Requisitos;
- Relação entre **Requisito**, **User Story** e **Tarefas**;
- Gestão do Backlog;
- Gestão de Prioridade e Estimativa de complexidade;
- **Definition of Done (DoD)**;
- Framework ágil **Scrum** no desenvolvimento Front-end;
- Planejamento prático de tarefas, Kanban, Sprints e branches.

---

## 🧠 Resumo Didático

### 1. Por que Gerenciar um Projeto Front-End?

Projetos de interface crescem rapidamente em número de telas, estados, integrações e componentes. Sem gestão estruturada surgem problemas recorrentes, enquanto a adoção de boas práticas de planejamento traz previsibilidade:

| Sem Planejamento | Com Processo de Gestão |
|---|---|
| Tarefas esquecidas e requisitos confusos | Responsabilidades claras na equipe |
| Retrabalho constante e atrasos | Prioridades bem definidas |
| Conflitos frequentes no Git | Entregas incrementais e contínuas |
| Problemas de integração e falta de visibilidade | Acompanhamento transparente do progresso |

### 2. De Requisitos a Tarefas Executáveis

O fluxo de engenharia parte de uma necessidade do produto e a decompõe até unidades técnicas verificáveis:

- **Requisito:** declara o que o sistema deve permitir (ex.: *O sistema deve permitir o gerenciamento de tarefas*).
- **User Story (História de Usuário):** descreve a funcionalidade sob a perspectiva de quem utiliza a aplicação (*"Como [perfil], quero [ação], para [benefício]"*).
- **Tarefas:** passos técnicos concretos de implementação (*criar formulário, criar componente, validar campos, integrar API, criar testes*).

### 3. Backlog, Priorização e Estimativa

- **Backlog do Produto:** lista viva que reúne funcionalidades, melhorias e correções necessárias para construir e evoluir a aplicação.
- **Priorização:** define o que deve ser desenvolvido primeiro considerando valor ao usuário, objetivos do MVP e dependências técnicas.
- **Estimativa:** avalia a complexidade relativa de cada atividade antes que a equipe assuma um ciclo de entrega (*Sprint*).

### 4. Scrum e Definition of Done (DoD)

- **Scrum:** framework ágil iterativo e incremental baseado em ciclos curtos (**Sprints**), inspeção frequente e adaptação contínua.
- **Definition of Done (Critérios de Conclusão):** conjunto de verificações obrigatórias para que um item seja considerado realmente pronto — incluindo código implementado, revisão de código (*Pull Request*), testes executados, responsividade validada e integração concluída.

---

## 💻 Exemplo Explicado — Decomposição Ágil no Front-end

```markdown
### Requisito Funcional
RF01 — O sistema deve permitir o gerenciamento de tarefas pelo usuário.

### User Story
Como estudante,
quero cadastrar e filtrar minhas tarefas por prioridade,
para organizar minhas entregas semanais sem perder prazos.

### Tarefas Técnicas (Kanban)
- [x] Criar componente `TaskForm` com campos controlados
- [x] Implementar validação de campos obrigatórios
- [x] Criar componente `TaskCard` reutilizável via props
- [x] Persistir lista de tarefas e validar responsividade mobile/desktop

### Definition of Done (DoD)
- Código revisado em branch dedicada (`feat/gerenciamento-tarefas`);
- Build de produção (`npm run build`) executado sem erros;
- Layout testado em celular (360px) e desktop (1280px).
```

---

## 🛠️ Atividade Solicitada na Aula

- **Planejamento e Gestão de Projeto Front-end:**
  1. Planejar a gestão das tarefas do projeto em grupo aplicando os conceitos estudados na aula;
  2. Estruturar **backlog, prioridades, tarefas, estimativas, Sprints, quadro Kanban, padrão de branches e critérios de conclusão (*Definition of Done*)**;
  3. Documentar todo o processo em um arquivo Markdown e utilizar o quadro criado para acompanhar o desenvolvimento.

---

## 🔗 Materiais, Artefatos Práticos e Referências

- 📄 **Material oficial da aula (PDF):** [Aula-06-Projetos-Front-End.pdf](./Aula-06-Projetos-Front-End.pdf)
- 📋 **Atividade prática documentada em Markdown:** [planejamento-gestao-projeto.md](./planejamento-gestao-projeto.md)
- 📑 **Modelo estruturado de apoio ao Mini TCC (ABNT) do Projeto Final:** [modelo-mini-tcc-abnt.md](./modelo-mini-tcc-abnt.md)
- 🚀 **Aplicação prática de gestão em equipe no Hackathon (Git Flow, Requisitos, User Stories e Kanban):** [🔗 Enzootomas/cuida-facil](https://github.com/Enzootomas/cuida-facil) | [🌐 Ver online](https://cuida-facil-qckjx199m-enzootomas-projects.vercel.app)
- 📚 **Repositórios complementares do professor:**
  - [aula-gestao](https://github.com/deivisontakatu/aula-gestao)
  - [aula-gestao-produto](https://github.com/deivisontakatu/aula-gestao-produto)
  - [aula-scrum](https://github.com/deivisontakatu/aula-scrum)

---

[⬅️ Voltar ao índice principal](../README.md)
