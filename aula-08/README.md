# Aula 08 — Projeto React

Na Aula 08 realizamos inicialmente uma revisão estruturada da linguagem **JavaScript** e da manipulação do **DOM**, avançando em seguida para a construção prática de interfaces declarativas com **React**, cobrindo **JSX**, **Componentes**, **Props**, **Virtual DOM e Reconciliação**, **Listas e Keys** e **Renderização Condicional**.

---

## 📌 Conteúdos Estudados

### Parte 1 — Revisão de JavaScript e DOM
- Formas de inclusão do JavaScript (interno com `<script>`, arquivo externo com `src` e eventos);
- Declaração de variáveis e escopo (`var`, `let` e `const`) e diferenciação *case sensitive*;
- Tipos de dados (`String`, `Number`, `Boolean`, `Undefined`, `Null`, `Object`, `Array`, `Symbol`, `BigInt`) e `typeof`;
- Operadores aritméticos, de comparação (`===`, `!==`), lógicos (`&&`, `||`, `!`) e de atribuição;
- Estruturas condicionais (`if`, `else if`, `else`, operador ternário `? :`) e de repetição (`for`, `while`, `do...while`, `break`, `continue`);
- Funções tradicionais e *arrow functions*, arrays (`forEach`, `filter`, `map`) e objetos (`this`);
- Seleção e manipulação manual do DOM (`getElementById`, `querySelector`, `querySelectorAll`, `textContent`, `value`, `classList`, `createElement`, `appendChild`, `addEventListener`).

### Parte 2 — Fundamentos de Projeto React
- **JSX:** sintaxe, interpolação de expressões com `{}` e diferenças em relação ao HTML (`className`, `htmlFor`, fechamento de tags `<img />`, elemento raiz / Fragment);
- **Componentes:** criação de funções iniciadas com letra maiúscula, árvore hierárquica de componentes, composição e reutilização;
- **Props:** passagem unidirecional de dados do componente pai para o filho (strings, números, booleanos, arrays, objetos, funções e elementos React);
- **DOM x Virtual DOM:** descrição declarativa da interface, renderização e processo de **reconciliação**;
- **Listas e Keys:** transformação de arrays em elementos JSX com `map()`, filtragem com `filter()` e importância de chaves `key` estáveis;
- **Renderização Condicional:** controle do que aparece na tela com `if / return` antecipado, operador ternário (`? :`) e `&&` lógico.

---

## 🧠 Resumo Didático

### 1. JSX e Componentização

O **JSX** permite descrever a estrutura visual diretamente em JavaScript, unindo marcação e lógica dentro de **componentes funcionais** independentes. Dividir uma página em componentes menores (como `Sidebar`, `StatCard`, `TaskCard` e `TaskForm`) evita repetição, organiza a árvore da aplicação e facilita a manutenção.

### 2. Fluxo de Dados com Props

As **Props** (*properties*) funcionam como parâmetros de entrada recebidos pelo componente filho. A estrutura visual do componente permanece a mesma enquanto o conteúdo exibido muda conforme os dados enviados pelo componente pai, mantendo o fluxo de dados explícito e previsível.

### 3. Virtual DOM, Listas e Keys

Em vez de manipular elementos manualmente com `querySelector`, no React o desenvolvedor declara como a interface deve parecer para cada estado. Na **reconciliação**, o React compara a nova descrição de elementos em memória (**Virtual DOM**) com a anterior e aplica ao DOM real apenas as diferenças necessárias. Em listas geradas com `map()`, a propriedade `key` (como `key={item.id}`) identifica cada elemento de forma única entre renderizações.

### 4. Renderização Condicional

Permite adaptar a interface conforme os dados disponíveis — exibindo, por exemplo, mensagens de lista vazia (`resultados.length === 0`), indicadores de carregamento ou cartões estilizados de acordo com o status de cada item.

---

## 💻 Exemplos Explicados

### Exemplo 1 — Componente Reutilizável com Props e JSX

```jsx
function CardConceito({ titulo, descricao }) {
  return (
    <article className="card-conceito">
      <h2>{titulo}</h2>
      <p>{descricao}</p>
    </article>
  );
}

// Reutilização no componente pai:
<CardConceito titulo="JSX" descricao="Extensão de sintaxe para descrever interfaces." />
<CardConceito titulo="Props" descricao="Dados enviados do componente pai para o filho." />
```

### Exemplo 2 — Lista Filtrada com `key` e Renderização Condicional

```jsx
function ListaResultados({ resultados }) {
  if (resultados.length === 0) {
    return <p>Nenhum resultado encontrado.</p>;
  }

  return (
    <ul>
      {resultados.map((item) => (
        <li key={item.id}>{item.nome}</li>
      ))}
    </ul>
  );
}
```

---

## 🛠️ Atividade Solicitada na Aula

- **Desenvolvimento de Aplicação React (Parte 1):**
  - Desenvolver uma aplicação React aplicando todos os conceitos estudados na aula: **JSX**, **componentes**, **props**, **Virtual DOM**, **listas com keys** e **renderização condicional**;
  - Publicar em repositório público no GitHub acompanhado de `README.md` descrevendo o projeto, suas funcionalidades e onde cada conceito foi aplicado.

---

## 🔗 Materiais, Projetos e Referências

- 📄 **Material oficial da aula (PDF):** [Aula-08-Projeto-React.pdf](./Aula-08-Projeto-React.pdf)
- 💻 **Projeto prático desenvolvido (TaskFlow React):** [🔗 Enzootomas/react-taskflow](https://github.com/Enzootomas/react-taskflow) *(Integra os conceitos das Aulas 08 e 09; deploy na Vercel pendente de publicação manual)*
- 📚 **Materiais complementares do professor:**
  - [Revisão JavaScript — aula-javascript](https://github.com/deivisontakatu/aula-javascript)
  - [Conceitos React — aula-react](https://github.com/deivisontakatu/aula-react)
  - [ Código de exemplo — projeto-react](https://github.com/deivisontakatu/projeto-react)
  - [Aplicação de referência publicada](https://projeto-react-five-swart.vercel.app/)

---

[⬅️ Voltar ao índice principal](../README.md)
