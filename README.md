# Catálogo de Livros — Trabalho Prático DGT2809

Trabalho prático da disciplina **DGT2809 – Aprofundamento em Desenvolvimento Front-End** (Estácio).

Aplicação Angular (arquitetura com `NgModule`) que exibe um catálogo de livros, permite excluir e cadastrar novos livros, usando serviços injetáveis, componentes, formulários (`FormsModule` / `ngModel`) e navegação interna (Angular Router). Estilo com Bootstrap 5 via CDN.

## Estrutura

| Arquivo | Descrição |
|---|---|
| `src/app/editora.ts` | Entidade Editora (`codEditora`, `nome`) |
| `src/app/livro.ts` | Entidade Livro (`codigo`, `codEditora`, `titulo`, `resumo`, `autores`) |
| `src/app/controle-editora.service.ts` | Serviço com `getEditoras` e `getNomeEditora` |
| `src/app/controle-livros.service.ts` | Serviço com `obterLivros`, `incluir` e `excluir` |
| `src/app/livro-lista/` | Componente da listagem (rota `/lista`) |
| `src/app/livro-dados/` | Componente do formulário de cadastro (rota `/dados`) |
| `src/app/app-routing.module.ts` | Rotas `lista`, `dados` e rota padrão |
| `src/app/app.module.ts` | Providers dos serviços e `FormsModule` |

## Como executar

Pré-requisito: Node.js 18.19+ instalado.

```bash
npm install
npx ng serve
```

Acesse `http://localhost:4200/`.

> Os dados ficam em memória: ao recarregar a página o catálogo volta aos 3 livros iniciais.
