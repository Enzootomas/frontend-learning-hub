# 📑 Guia e Estrutura Base — Relatório Acadêmico (Mini TCC ABNT)

Material de apoio elaborado estritamente a partir dos requisitos oficiais do documento `Atividade/Projeto.md` e das referências bibliográficas do **Plano de Ensino** do Prof. Me. Deivison S. Takatu, destinado à redação e revisão colaborativa pelos integrantes do grupo no **Projeto Final da Disciplina de Frameworks Front-End**.

> **Importante:** Este documento é um **modelo estrutural acadêmico**. Os campos sinalizados com `[PREENCHER PELO GRUPO]` devem ser completados exclusivamente com os dados reais do grupo, do tema aprovado pelo professor e dos testes efetivamente realizados pela equipe.

---

## ELEMENTOS PRÉ-TEXTUAIS (ABNT NBR 14724)

### Capa
- **Instituição:** Serviço Nacional de Aprendizagem Industrial — SENAI
- **Curso:** Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas
- **Título do Trabalho:** `[PREENCHER PELO GRUPO: Nome e subtítulo da aplicação web]`
- **Integrantes:** `[PREENCHER PELO GRUPO: Nomes completos em ordem alfabética]`
- **Cidade e Ano:** `[PREENCHER PELO GRUPO: Cidade - UF]`, 2026

### Folha de Rosto
- **Autores:** `[PREENCHER PELO GRUPO]`
- **Título:** `[PREENCHER PELO GRUPO]`
- **Natureza do Trabalho:** Relatório técnico-acadêmico (mini TCC) apresentado à disciplina de **Frameworks Front-End**, do Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas do SENAI, como requisito parcial de avaliação sob orientação do Prof. Me. Deivison S. Takatu.

### Resumo
Parágrafo único (150 a 250 palavras, voz ativa na terceira pessoa do singular, conforme ABNT NBR 6028) sintetizando:
1. Contexto e problema identificado;
2. Objetivo geral da aplicação web;
3. Metodologia de planejamento e tecnologias Front-end adotadas;
4. Solução desenvolvida (MVP);
5. Principais resultados obtidos na validação e conclusões.

**Palavras-chave:** Desenvolvimento Web. Frameworks Front-End. `[Framework utilizado, ex.: React]`. Interfaces Responsivas. `[Domínio do projeto]`.

### Sumário
1. Introdução  
2. Fundamentação Teórica  
3. Metodologia e Planejamento  
4. Desenvolvimento da Aplicação  
5. Resultados e Validação  
6. Considerações Finais  
Referências  

---

## ELEMENTOS TEXTUAIS

### 1. Introdução
- **1.1 Contextualização do tema:** importância das aplicações web responsivas e interativas no contexto escolhido pelo grupo.
- **1.2 Descrição do problema:** qual dificuldade real ou necessidade prática motivou a proposta.
- **1.3 Justificativa:** relevância técnica, acadêmica e prática da solução para o público-alvo.
- **1.4 Objetivo Geral:** planejar, desenvolver, documentar e validar a aplicação web `[NOME DO PROJETO]` utilizando tecnologias estudadas em Frameworks Front-End.
- **1.5 Objetivos Específicos:**
  - Levantar e priorizar os requisitos funcionais e não funcionais do Produto Mínimo Viável (MVP);
  - Projetar uma interface organizada, acessível e responsiva voltada ao público-alvo;
  - Implementar a aplicação com arquitetura baseada em componentes reutilizáveis;
  - Gerenciar o desenvolvimento colaborativo com backlog e versionamento Git/GitHub;
  - Validar os fluxos principais da aplicação por meio de cenários de teste documentados.
- **1.6 Organização do documento:** breve descrição do que é abordado nas seções 2 a 6.

### 2. Fundamentação Teórica
Relacionar cada conceito teórico diretamente às decisões tomadas no projeto (utilizando citações indiretas ou diretas conforme ABNT NBR 10520):
- **2.1 Desenvolvimento Front-End e Experiência do Usuário (UX):** papel da camada de interface, usabilidade, feedback visual e design de interação (EIS, 2015; PREECE; ROGERS; SHARP, 2013).
- **2.2 Estilização Moderna, Responsividade e Frameworks CSS:** adaptação a múltiplos dispositivos (mobile, tablet e desktop), sistemas de grid/flexbox e produtividade na padronização visual (SOUZA, 2018).
- **2.3 Arquitetura Baseada em Componentes, Estado e Rotas:** benefícios do uso de frameworks/bibliotecas Front-end na modularização, reutilização de código, gerenciamento reativo de estado e navegação em *Single Page Applications* (EIS, 2015; MACHADO, 2021).
- **2.4 Versionamento e Gestão Ágil de Software:** rastreabilidade de código com Git/GitHub, organização incremental em backlog e validação contínua de entregas.

### 3. Metodologia e Planejamento
- **3.1 Caracterização da solução e público-alvo:** `[PREENCHER PELO GRUPO]`.
- **3.2 Levantamento de requisitos e escopo do MVP:** tabela de Requisitos Funcionais (`RF`) e Requisitos Não Funcionais (`RNF`) priorizados.
- **3.3 Gestão do backlog e divisão de responsabilidades:** ferramenta utilizada (GitHub Projects / Trello), colunas do Kanban, priorização e quadro real de contribuições por integrante (`[PREENCHER PELO GRUPO]`).
- **3.4 Estratégia de versionamento e colaboração:** uso de branches, padrão de mensagens de commit e revisão por Pull Requests.
- **3.5 Procedimentos de validação:** critérios utilizados para testar formulários, fluxos principais, mensagens de erro e responsividade.

### 4. Desenvolvimento da Aplicação
- **4.1 Visão geral e funcionalidades implementadas:** descrição objetiva do sistema entregue.
- **4.2 Tecnologias utilizadas e justificativas técnicas:** linguagem, biblioteca/framework Front-end, estilização, roteamento, armazenamento (`localStorage` ou consumo de API) e hospedagem.
- **4.3 Arquitetura de pastas e árvore de componentes:** diagrama da estrutura `src/` e explicação do fluxo de dados (`props` e `state`).
- **4.4 Fluxos de navegação e interfaces:** apresentação das telas desenvolvidas com ilustrações numeradas e tituladas conforme ABNT (*Figura 1 — Tela inicial da aplicação / Fonte: Elaborado pelos autores (2026)*).
- **4.5 Decisões técnicas, acessibilidade e responsividade:** escolhas relevantes adotadas pela equipe.

### 5. Resultados e Validação
- **5.1 Quadro de cenários de teste executados:**

| ID | Cenário Testado | Entrada / Ação | Resultado Esperado | Resultado Obtido | Status |
|---|---|---|---|---|---|
| CT01 | `[PREENCHER PELO GRUPO]` | `[Ação real]` | `[Comportamento esperado]` | `[Evidência real verificada]` | `[Aprovado/Ajustado]` |

- **5.2 Comparação entre objetivos planejados e MVP alcançado:** análise crítica baseada nas evidências reais.
- **5.3 Problemas encontrados, soluções adotadas e limitações conhecidas:** transparência sobre o que ficou fora do escopo do MVP.

### 6. Considerações Finais
- Retomada do objetivo geral e síntese dos resultados alcançados;
- Principais aprendizados técnicos (componentização, estado, estilização responsiva, Git em equipe) e socioemocionais;
- Trabalhos futuros e evoluções possíveis para a aplicação.

---

## ELEMENTOS PÓS-TEXTUAIS — REFERÊNCIAS BASE (ABNT NBR 6023)

> Manter na versão final **somente** as obras efetivamente citadas ao longo do texto pelo grupo, acrescentando as documentações oficiais das tecnologias utilizadas no projeto:

EIS, Diego. **Guia front-end**: o caminho das pedras para ser um dev front-end. São Paulo: Casa do Código, 2015. E-book.

HARTCOPP, Patrícia Ferreira. **Métrica web**. São Paulo: Contentus, 2020. E-book.

MACHADO, Kheronn Khennedy. **Angular 11 e Firebase**: construindo uma aplicação integrada com a plataforma do Google. São Paulo: Casa do Código, 2021. E-book.

META PLATFORMS. **React Documentation**. 2026. Disponível em: https://react.dev/. Acesso em: 25 nov. 2026.

MOZILLA DEVELOPER NETWORK (MDN). **MDN Web Docs — Tecnologias Web para Desenvolvedores**. 2026. Disponível em: https://developer.mozilla.org/pt-BR/. Acesso em: 25 nov. 2026.

PREECE, Jennifer; ROGERS, Yvonne; SHARP, Helen. **Design de interação**: além da interação homem-computador. 3. ed. Porto Alegre: Bookman, 2013.

SOUZA, Natan. **Bootstrap 4**: conheça a biblioteca front-end mais utilizada no mundo. São Paulo: Casa do Código, 2018. E-book.

TAILWIND LABS. **Tailwind CSS Documentation**. 2026. Disponível em: https://tailwindcss.com/docs. Acesso em: 25 nov. 2026.

---

[⬅️ Voltar para a Aula 06](./README.md) | [⬅️ Voltar ao índice principal](../README.md)
