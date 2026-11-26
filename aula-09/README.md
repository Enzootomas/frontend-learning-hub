# Aula 09 — Projeto React 02

Na Aula 09 demos continuidade ao desenvolvimento de aplicações completas com **React**, aprofundando o gerenciamento de estado com **Hooks (`useState`)**, **Formulários Controlados**, sincronização com sistemas externos via **`useEffect`**, **Consumo de APIs com `fetch`** e navegação entre páginas em *Single Page Applications* com **React Router**.

---

## 📌 Conteúdos Estudados

- **State e `useState`:** por que variáveis locais comuns não atualizam a interface, regras dos Hooks e atualização reativa de estado;
- **Formulários em React:** campos controlados (`value` + `onChange`), evento `onSubmit`, uso de `preventDefault()` e validação de entradas;
- **Hook `useEffect`:** efeitos colaterais fora da renderização, array de dependências (`[]`, `[valor]`) e função de limpeza (*cleanup*);
- **Consumo de APIs:** requisições assíncronas com `fetch()` (`GET` e `POST`), leitura de JSON (`response.json()`), verificação de `response.ok`, tratamento de erros (`try / catch`), estados de carregamento e cuidados com CORS e chaves secretas;
- **React Router:** roteamento por URL com `BrowserRouter`, `Routes`, `Route`, navegação declarativa com `Link` / `NavLink` e leitura de parâmetros dinâmicos com `useParams()`.

---

## 🧠 Resumo Didático

### 1. State e o Hook `useState`

Variáveis locais comuns são recriadas a cada execução da função e suas alterações não disparam uma nova renderização. O Hook `useState(valorInicial)` retorna um par `[estadoAtual, atualizarEstado]`, preservando a informação entre renderizações e instruindo o React a atualizar a interface sempre que a função atualizadora é chamada.

### 2. Formulários Controlados e `preventDefault()`

Em um **campo controlado**, o estado do React é a única fonte da verdade: o atributo `value` exibe o valor do estado e o evento `onChange` atualiza esse estado a cada tecla digitada (`e.target.value`). No envio do formulário (`onSubmit`), `event.preventDefault()` impede o recarregamento padrão do navegador, permitindo validar os dados e atualizar a interface diretamente no React.

### 3. Sincronização e Limpeza com `useEffect`

O `useEffect` conecta o componente a recursos externos ao ciclo puro de renderização — como atualizar `document.title`, salvar dados no `localStorage`, registrar *listeners* ou buscar dados em uma API. Quando o efeito cria recursos persistentes (eventos de janela, `setInterval` ou requisições em andamento com `AbortController`), deve retornar uma **função de limpeza** para liberá-los quando o componente desmonta ou as dependências mudam.

### 4. Consumo de APIs e Roteamento com React Router

- **`fetch()` + Estados de Interface:** ao consultar serviços externos, boas práticas exigem verificar `if (!response.ok)`, capturar falhas de rede com `try / catch` e representar claramente os estados de **carregamento**, **sucesso**, **lista vazia** e **erro**.
- **React Router (`react-router-dom`):** organiza aplicações de múltiplas telas associando caminhos de URL (`/`, `/tarefas`, `/tarefas/:id`, `/usuarios`) a componentes específicos, navegando instantaneamente com `<Link>` / `<NavLink>` e extraindo parâmetros variáveis com `useParams()`.

---

## 💻 Exemplos Explicados

### Exemplo 1 — Formulário Controlado com `useState` e `preventDefault()`

```jsx
import { useState } from "react";

function FormularioTarefa({ aoSalvar }) {
  const [titulo, setTitulo] = useState("");

  function enviar(evento) {
    evento.preventDefault();
    if (!titulo.trim()) return;
    aoSalvar(titulo.trim());
    setTitulo("");
  }

  return (
    <form onSubmit={enviar}>
      <input
        value={titulo}
        onChange={(e) => setTitulo(e.target.value)}
        placeholder="Nova tarefa..."
      />
      <button type="submit">Adicionar</button>
    </form>
  );
}
```

### Exemplo 2 — Busca em API com `useEffect`, Limpeza e Tratamento de Erros

```jsx
useEffect(() => {
  const controller = new AbortController();

  async function carregarUsuarios() {
    try {
      const resposta = await fetch("https://jsonplaceholder.typicode.com/users", {
        signal: controller.signal,
      });
      if (!resposta.ok) throw new Error("Erro na consulta");
      const dados = await resposta.json();
      setUsuarios(dados);
    } catch (erro) {
      if (erro.name !== "AbortError") setStatus("error");
    }
  }

  carregarUsuarios();
  return () => controller.abort();
}, []);
```

### Exemplo 3 — Rotas e Parâmetros com React Router (`useParams`)

```jsx
import { BrowserRouter, Routes, Route, Link, useParams } from "react-router-dom";

function DetalheTarefa() {
  const { id } = useParams();
  return <h1>Detalhes da tarefa #{id}</h1>;
}
```

---

## 🛠️ Atividade Solicitada na Aula

- **Desenvolvimento de Aplicação React (Parte 2):**
  - Desenvolver uma aplicação React utilizando todos os conceitos estudados na aula: **State e `useState`**, **Formulários**, **`useEffect`**, **Consumo de APIs** e **React Router**;
  - Disponibilizar em repositório público no GitHub com `README.md` detalhando a descrição, as funcionalidades e o mapeamento dos conceitos aplicados.

---

## 🔗 Materiais, Projetos e Referências

- 📄 **Material oficial da aula (PDF):** [Aula-09-Projeto-React-02.pdf](./Aula-09-Projeto-React-02.pdf)
- 💻 **Projeto prático desenvolvido (DevFeed React 02 — Hooks, API GET/POST e React Router):** [🔗 Repositório](https://github.com/Enzootomas/projeto-react-02)
- 💻 **Projeto complementar integrado (TaskFlow React):** [🔗 Repositório](https://github.com/Enzootomas/react-taskflow)
- 📚 **Materiais complementares do professor:**
  - [Conceitos React — aula-react](https://github.com/deivisontakatu/aula-react)
  - [Código de exemplo — projeto-react](https://github.com/deivisontakatu/projeto-react)
  - [Aplicação de referência publicada](https://projeto-react-five-swart.vercel.app/)

---

[⬅️ Voltar ao índice principal](../README.md)
