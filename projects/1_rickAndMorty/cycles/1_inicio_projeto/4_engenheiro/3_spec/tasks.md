# ⚙️ Tasks Técnicas — Painel Rick and Morty

> Status: SPEC (documento final — entrada para o Desenvolvedor)

---

## Contexto

Implementar o painel conforme a arquitetura definida. Arquivo único `index.html` com HTML, CSS e JS embutidos.

---

## TASK-01 — Estrutura HTML Base

Criar o esqueleto do `index.html`:

```html
<header>         → título "👽 Rick and Morty API"
<section#filtros> → input[type=text] + select + button
<div#grid>        → onde os cards serão injetados
<div#paginacao>   → button#btn-prev + span#info-pagina + button#btn-next
```

**Critério de aceite:** HTML válido, semântico, carrega no browser sem erros.

---

## TASK-02 — CSS Completo

Implementar todos os estilos usando as variáveis definidas na arquitetura:

- Layout geral: background escuro, fonte clara
- Filtros: alinhados em linha, responsivos
- Cards: grid de 4 colunas (desktop), 2 (tablet), 1 (mobile)
- Card: imagem no topo, nome em negrito, badge colorido para status
- Paginação: botões centralizados, desabilitados quando inativo

**Critério de aceite:** Visual agradável, sem overflow, responsivo.

---

## TASK-03 — Lógica JavaScript

Implementar as funções conforme a arquitetura:

### `buscarPersonagens(pagina, nome, status)`
```js
// Monta URL, chama fetch, chama render e pagina
// Em caso de erro 404, exibe "Nenhum personagem encontrado"
```

### `renderizarCards(results)`
```js
// Mapeia results[] para cards HTML
// Badge: classe .alive / .dead / .unknown conforme status
```

### `atualizarPaginacao(info)`
```js
// info.prev === null → desabilitar btn-prev
// info.next === null → desabilitar btn-next
// Atualizar texto "Página X de Y"
```

### Event listeners
```js
// btn-buscar → click → buscarPersonagens(1, inputNome, selectStatus)
// input-nome → keydown Enter → mesma ação
// select-status → change → buscarPersonagens(1, inputNome, selectStatus)
// btn-prev → click → paginaAtual-- → buscarPersonagens
// btn-next → click → paginaAtual++ → buscarPersonagens
```

**Critério de aceite:** Todos os filtros e paginação funcionando sem reload.

---

## Ordem de Implementação Sugerida

1. TASK-01 → estrutura HTML
2. TASK-03 → JS funcional (sem estilo)
3. TASK-02 → CSS (estilizar o que já funciona)
