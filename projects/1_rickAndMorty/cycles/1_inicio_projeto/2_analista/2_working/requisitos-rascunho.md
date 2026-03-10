# 🕵️ Requisitos em Rascunho — Analista

> Status: WORKING (em refinamento)

---

## Funcionalidades Identificadas

### RF01 — Listagem de Personagens
- Exibir personagens em cards (foto, nome, status, espécie)
- Carregar 20 personagens por vez (paginação da API)

### RF02 — Filtro por Nome
- Campo de texto para busca
- Filtro aplicado ao digitar (ou ao pressionar Enter)

### RF03 — Filtro por Status
- Seletor com opções: Todos, Alive, Dead, Unknown
- Pode ser combinado com o filtro de nome

### RF04 — Paginação
- Botões "Anterior" e "Próximo"
- Exibir número da página atual

### RF05 — Indicador de Status Visual
- 🟢 Alive → verde
- 🔴 Dead → vermelho
- ⚫ Unknown → cinza

## Regras de Negócio

- RN01: Se a API retornar erro (personagem não encontrado), exibir mensagem amigável
- RN02: Filtros devem ser resetados ao navegar de página

## Campos da API a Usar

| Campo | Usado em |
|---|---|
| `name` | Card do personagem |
| `status` | Badge colorido |
| `species` | Card do personagem |
| `image` | Foto no card |
| `location.name` | Card do personagem |
