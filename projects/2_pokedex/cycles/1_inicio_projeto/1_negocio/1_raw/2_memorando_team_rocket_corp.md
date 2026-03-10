# 📜 Memorando Interno — Team Rocket Corp.
**Classificação:** CONFIDENCIAL (não mostrar ao Professor Carvalho)
**De:** Giovani, CEO
**Para:** Equipe de Estratégia e Produto
**Data:** 10 de março, após reunião em Paleta
**CC:** Jessie, James, Meowth (para eles pararem de atrapalhar e contribuírem)

---

## Assunto: Strategic Product Brief — Pokédex Web

Senhores,

Acabei de sair de uma reunião produtiva com o Professor Carvalho. Produtiva *para nós*, pelo menos.

### Contexto de Negócio

O mundo tem mais de 800 espécies de Pokémon hoje. A única forma de consultar dados é:

1. **Pokédex Física** — cara, quebra fácil, o Ash perdeu a dele umas 4 vezes
2. **Livros do Professor Carvalho** — 600 páginas, formatação de 1989
3. **Memória do Brock** — surpreendentemente boa, mas ele está sempre distraído

**Gap identificado:** *Não existe nenhuma solução web moderna, gratuita e acessível.*

Quem controlar essa informação, controla o mercado de Pokémon raros. *(Entre nós.)*

### Necessidades de Produto

| Funcionalidade | Prioridade | Justificativa |
|---|---|---|
| Busca por nome/número | 🔴 Alta | Localizar espécies-alvo rapidamente |
| Imagem do Pokémon | 🔴 Alta | Identificação visual para captura |
| Tipos do Pokémon | 🟡 Média | Estratégia de batalha e vantagens |
| Stats (HP, Ataque...) | 🟡 Média | Avaliar valor de mercado |
| Cores por tipo | 🟢 Baixa | UX bonita pra enganar investidores |

### Premissa Técnica

Existe uma **API pública e gratuita** chamada PokéAPI (`pokeapi.co`).
Ela já tem tudo. Nome, número, imagem, tipos, stats. Tudo.

Não precisamos construir banco de dados. Só precisamos de uma **interface web decente em cima dela**.

### Estimativa

- Desenvolvimento: ~1 semana com IA assistindo
- Custo de infraestrutura: **R$ 0** (GitHub Pages)
- Custo da API: **R$ 0** (pública e gratuita)
- Total de investimento real necessário: **quase nada**

*Mas peço R$ 1.000.000 ao Carvalho assim mesmo. Ele aceita se eu falar "pela ciência".*

### Próximo Passo

Envolver equipe de desenvolvimento. Assim que tivermos os requisitos formais (o Carvalho chama de "Analista"), começamos a construção.

> **Lembrete:** Se o Ash aparecer perguntando sobre o projeto, digam que é um sistema de *preservação ecológica de Pokémon selvagens*. Ele vai adorar.

— G.

*P.S.: Jessie e James, se aparecerem no standup de amanhã usando fantasia, estão demitidos. De novo.*
