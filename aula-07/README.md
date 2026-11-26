# Aula 07 — Frameworks CSS

Na Aula 07 revisamos os fundamentos essenciais das folhas de estilo (**Cascading Style Sheets — CSS**), aprofundamos o **Box Model**, o layout unidimensional com **Flexbox** e a construção de **layouts responsivos**, avançando em seguida para o estudo dos **Frameworks CSS**, com ênfase prática no **Tailwind CSS** e sua abordagem **Utility-First**.

---

## 📌 Conteúdos Estudados

- Estrutura da regra CSS: `seletor { propriedade: valor; }`;
- Formas de aplicação do CSS: **In-line**, **Interno** (`<style>`) e **Externo** (`<link>`);
- Principais propriedades visuais e estruturais (`color`, `background-color`, `font-family`, `font-size`, `margin`, `padding`, `border`, `width`, `height`, `display`, `position`, `top/right/bottom/left`, `text-align`);
- Diferença prática entre seletores de **Classe (`.classe`)** e **ID (`#id`)**;
- **Box Model** (*Content*, *Padding*, *Border* e *Margin*);
- **Flexbox** (`flex-direction`, `justify-content`, `align-items`, `flex-wrap`, `gap` e alinhamentos);
- **Layouts Responsivos** e configuração da meta tag `viewport`;
- Conceito e pilares de um **Framework CSS** (Layout, Estilos e Componentes);
- **Tailwind CSS v4**: conceito *Utility-First*, importação via Play CDN e Tailwind CLI, integração com frameworks e extensão **Tailwind CSS IntelliSense**.

---

## 🧠 Resumo Didático

### 1. Formas de Aplicação do CSS

| Abordagem | Como funciona | Quando utilizar |
|---|---|---|
| **CSS In-line** | Atributo `style="..."` diretamente na tag HTML | Apenas testes rápidos ou ajustes pontuais |
| **CSS Interno** | Bloco `<style>` dentro do `<head>` do HTML | Páginas isoladas ou protótipos simples |
| **CSS Externo** | Arquivo `.css` vinculado por `<link rel="stylesheet" href="style.css">` | **Padrão recomendado** para organizar e reutilizar estilos |

### 2. Box Model (Modelo de Caixas)

Todo elemento HTML gera uma caixa retangular composta por quatro camadas concêntricas:
1. **Content:** área central onde textos e imagens são exibidos (`width`, `height`);
2. **Padding:** preenchimento interno entre o conteúdo e a borda;
3. **Border:** linha de contorno que envolve o `padding` e o conteúdo;
4. **Margin:** espaçamento externo que separa o elemento dos vizinhos.

### 3. Flexbox e Layouts Responsivos

O **Flexbox** organiza elementos em linhas (`row`) ou colunas (`column`), facilitando a distribuição de espaço (`justify-content`), o alinhamento no eixo transversal (`align-items`), a quebra automática de linha (`flex-wrap`) e o espaçamento uniforme (`gap`). Combinado à meta tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">` e *media queries*, garante adaptação fluida a celulares, tablets e computadores.

### 4. Frameworks CSS e Tailwind CSS (Utility-First)

Um **Framework CSS** oferece um sistema padronizado de layout, tokens visuais e utilitários que elimina a repetição manual de regras básicas. Enquanto bibliotecas tradicionais entregam componentes fechados (como Bootstrap, Bulma e Foundation), o **Tailwind CSS** adota o paradigma **Utility-First**: pequenas classes atômicas com responsabilidade única (`p-6`, `bg-blue-600`, `text-white`, `rounded-lg`, `md:grid-cols-3`) combinadas diretamente nos elementos para compor qualquer interface com rapidez, consistência e design *Mobile First*.

---

## 💻 Exemplos Explicados

### Exemplo 1 — Box Model e Container Flexbox em CSS Externo

```css
.box-model {
  width: 250px;
  padding: 20px;
  border: 2px solid #38bdf8;
  margin: 16px auto;
}

.galeria-responsiva {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: stretch;
  gap: 16px;
}
```

### Exemplo 2 — Componente Estilizado com Tailwind CSS v4

```html
<!-- Importação Play CDN (testes rápidos) ou @import "tailwindcss"; via CLI/Vite -->
<article class="p-6 bg-white rounded-xl shadow-md flex flex-col gap-3">
  <h2 class="text-xl font-bold text-slate-900">Card Utility-First</h2>
  <p class="text-sm text-slate-600">Uma utility = uma responsabilidade.</p>
  <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold">
    Enviar
  </button>
</article>
```

---

## 🛠️ Atividades Solicitadas na Aula

1. **Atividade 01 — CSS Externo, Box Model e Flexbox:**
   - Criar um projeto com `index.html` e `style.css` vinculado de forma externa via `<link>`;
   - Adicionar **20 elementos** atribuindo valores em todas as propriedades de *Content*, *Padding*, *Border* e *Margin*;
   - Aplicar **20 propriedades de Flexbox** para organizar os elementos de forma responsiva.
2. **Atividade 02 — Projeto com Tailwind CSS (30+ classes):**
   - Criar um projeto utilizando pelo menos **30 classes diferentes do Tailwind CSS** cobrindo cores, tipografia, espaçamentos, dimensões, bordas, posicionamento, flexbox, grid e responsividade;
   - Documentar em Markdown com lista das classes utilizadas e suas respectivas funções.

---

## 🔗 Materiais, Projetos e Referências

- 📄 **Material oficial da aula (PDF):** [Aula-07-Frameworks-CSS.pdf](./Aula-07-Frameworks-CSS.pdf)
- 💻 **Projeto prático — Atividade 01 (CSS Externo, Box Model & Flexbox):** [🔗 Repositório](https://github.com/Enzootomas/projeto-css-flexbox)
- 💻 **Projeto prático — Atividade 02 (Tailwind CSS v4 — 45+ classes):** [🔗 Repositório](https://github.com/Enzootomas/projeto-tailwind-css)
- 📚 **Materiais de referência do professor e documentação oficial:**
  - [Repositório complementar — aula-css](https://github.com/deivisontakatu/aula-css)
  - [Repositório complementar — aula-tailwind](https://github.com/deivisontakatu/aula-tailwind)
  - [Repositório complementar — aula-bootstrap](https://github.com/deivisontakatu/aula-bootstrap)
  - [Documentação oficial do Tailwind CSS](https://tailwindcss.com/docs)

---

[⬅️ Voltar ao índice principal](../README.md)
