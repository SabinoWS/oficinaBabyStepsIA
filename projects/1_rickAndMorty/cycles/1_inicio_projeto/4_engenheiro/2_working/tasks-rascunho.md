# ⚙️ Tasks em Rascunho — Engenheiro

> Status: WORKING (organizando e detalhando as tasks)

---

## Épico: Painel Rick and Morty

### TASK-01 — Estrutura HTML base
- [ ] Criar `index.html` com head, header, seção de filtros, grid e paginação
- [ ] Meta tags de charset e viewport

### TASK-02 — Estilização CSS
- [ ] Definir variáveis CSS (cores, espaçamentos)
- [ ] Estilo do header
- [ ] Estilo dos filtros (input + select + botão)
- [ ] Estilo dos cards (foto, nome, badge de status)
- [ ] Grid responsivo de cards
- [ ] Estilo da paginação

### TASK-03 — Função buscarPersonagens()
- [ ] Montar URL com query params dinâmicos
- [ ] Chamar fetch com async/await
- [ ] Tratar erro de rede e 404
- [ ] Chamar renderizarCards e atualizarPaginacao

### TASK-04 — Função renderizarCards()
- [ ] Mapear array de results para HTML de cards
- [ ] Badge de status com cor dinâmica via classe CSS
- [ ] Injetar no `#grid`
- [ ] Exibir mensagem se results vazio

### TASK-05 — Paginação
- [ ] Função atualizarPaginacao(info) 
- [ ] Habilitar/desabilitar botões anterior/próximo
- [ ] Exibir "Página X de Y"

### TASK-06 — Filtros
- [ ] Event listener no input (Enter) e no select (change)
- [ ] Resetar para página 1 ao filtrar
