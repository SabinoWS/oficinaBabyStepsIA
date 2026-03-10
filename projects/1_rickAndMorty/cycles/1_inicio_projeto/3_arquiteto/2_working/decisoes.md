# 🏛️ Decisões Técnicas — Arquiteto

> Status: WORKING (em refinamento)

---

## Stack Decidida

| Tecnologia | Decisão | Motivo |
|---|---|---|
| HTML | Semântico, arquivo único | Simplicidade para a oficina |
| CSS | Variáveis CSS + Flexbox/Grid | Flexível sem framework |
| JavaScript | Vanilla ES6+ (async/await) | Sem dependências externas |

## Estrutura do Código

```
index.html
 └── <style>     → estilos globais, variáveis CSS, cards
 └── <body>      → header, filtros, grid de cards, paginação
 └── <script>    → lógica de fetch, renderização, eventos
```

## Decisões de Arquitetura

1. **Estado local simples:** variáveis globais para `paginaAtual`, `filtroNome` e `filtroStatus`
2. **Renderização:** função `renderizarCards(data)` que monta o HTML dos cards via string template
3. **API calls:** função `buscarPersonagens()` monta a URL com os filtros e chama o fetch
4. **Sem debounce:** filtro por nome só dispara ao pressionar Enter (evita chamadas desnecessárias)

## Paleta de Cores

```css
--bg: #111;
--card-bg: #1e1e1e;
--accent: #00b4d8;
--alive: #00b341;
--dead: #e63946;
--unknown: #6c757d;
```
