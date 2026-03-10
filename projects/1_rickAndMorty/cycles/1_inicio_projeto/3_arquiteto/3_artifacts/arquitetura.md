# 🏛️ Arquitetura Técnica — Painel Rick and Morty

> Status: SPEC (documento final — entrada para o Engenheiro)

---

## Visão Geral

Aplicação single-page em arquivo único `index.html`, sem dependências externas, consumindo a Rick and Morty REST API.

## Estrutura do Arquivo

```
index.html
 ├── <head>     → meta, title, <style>
 ├── <body>
 │    ├── header        → título da página
 │    ├── section#filtros → input nome + select status + botão buscar
 │    ├── div#grid      → cards dos personagens (CSS Grid)
 │    └── div#paginacao → botões anterior/próximo + indicador de página
 └── <script>   → toda a lógica JS
```

## Funções JavaScript

| Função | Responsabilidade |
|---|---|
| `buscarPersonagens()` | Monta URL com filtros, chama a API, chama `renderizarCards` |
| `renderizarCards(results)` | Gera HTML dos cards e injeta no `#grid` |
| `atualizarPaginacao(info)` | Habilita/desabilita botões, exibe "Página X de Y" |
| `resetarFiltros()` | Limpa campos e recarrega página 1 |

## Paleta de Cores (CSS Variables)

```css
:root {
  --bg: #111;
  --card-bg: #1e1e1e;
  --accent: #00b4d8;
  --text: #f0f0f0;
  --muted: #888;
  --alive: #00b341;
  --dead: #e63946;
  --unknown: #6c757d;
}
```

## Endpoint Principal

```
GET https://rickandmortyapi.com/api/character/?page={page}&name={name}&status={status}
```
