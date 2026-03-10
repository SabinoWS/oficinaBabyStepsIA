# 🕵️ Spec de Requisitos — Painel Rick and Morty

> Status: SPEC (documento final — entrada para o Arquiteto/Engenheiro)

---

## Histórias de Usuário

### HU-01 — Visualizar Personagens
**Como** visitante do painel,
**Quero** ver uma lista de personagens de Rick and Morty,
**Para** descobrir e explorar os personagens da série.

**Critérios de Aceite:**
- [ ] Exibe no mínimo 20 personagens por página
- [ ] Cada card mostra: foto, nome, status (com cor), espécie e localização
- [ ] O status usa badge colorido: 🟢 Alive, 🔴 Dead, ⚫ Unknown

---

### HU-02 — Filtrar por Nome
**Como** visitante do painel,
**Quero** buscar personagens pelo nome,
**Para** encontrar rapidamente um personagem específico.

**Critérios de Aceite:**
- [ ] Campo de texto visível no topo da página
- [ ] Filtro aplicado ao pressionar Enter ou clicar em buscar
- [ ] Exibe mensagem "Nenhum personagem encontrado" se resultado vazio

---

### HU-03 — Filtrar por Status
**Como** visitante do painel,
**Quero** filtrar personagens pelo status (vivo, morto, desconhecido),
**Para** ver apenas os personagens do tipo que me interessa.

**Critérios de Aceite:**
- [ ] Seletor com opções: Todos, Alive, Dead, Unknown
- [ ] Pode ser combinado com o filtro de nome
- [ ] Resetar filtros retorna à listagem completa

---

### HU-04 — Navegar entre Páginas
**Como** visitante do painel,
**Quero** navegar entre as páginas de personagens,
**Para** ver todos os 826 personagens disponíveis.

**Critérios de Aceite:**
- [ ] Botões "Anterior" e "Próximo" funcionais
- [ ] Botão "Anterior" desabilitado na primeira página
- [ ] Botão "Próximo" desabilitado na última página
- [ ] Exibe "Página X de Y" para orientação

---

## Campos da API Necessários

```
GET https://rickandmortyapi.com/api/character/?page={n}&name={name}&status={status}

Campos usados: id, name, status, species, location.name, image
```
