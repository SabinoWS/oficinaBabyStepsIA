# ⚙️ Análise Técnica — Engenheiro

> Status: RAW (análise inicial após leitura da spec e arquitetura)

---

Lendo spec do analista e arquitetura...

- Preciso de 4 funções principais: buscar, renderizar, paginar, resetar
- A paginação depende do campo `info.next` e `info.prev` da API
- O filtro de status usa query param: `?status=alive`
- Cards em CSS Grid, responsivo
- Cuidar com HTML injection ao usar template strings (dados vêm da API — confiáveis, mas bom hábito)
- Pensar no estado: preciso guardar página atual e filtros ativos

Tasks para quebrar:
1. Estrutura HTML base
2. Estilos CSS (variáveis, cards, layout)
3. Função buscarPersonagens
4. Função renderizarCards
5. Lógica de paginação
6. Filtros (nome e status)
7. Tratamento de erro (API sem resultado)
