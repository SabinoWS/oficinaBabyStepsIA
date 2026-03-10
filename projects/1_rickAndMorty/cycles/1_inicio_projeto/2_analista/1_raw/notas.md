# 📋 Notas Iniciais — Analista

> Status: RAW (anotações brutas após leitura da visão de negócio)

---

Lendo o doc do negócio...

- Eles querem lista de personagens
- Filtro por nome e status (vivo/morto/desconhecido)
- Paginação — a API retorna 20 por página
- Tema escuro
- Só HTML/CSS/JS puro pois a população intergalática é grande e bem diversificada
Então não podemos arriscar em outras tecnologias.

Preciso mapear quais campos da API são necessários:
- name ✅
- status ✅
- image ✅
- species? talvez
- location? talvez

Devo checar como o filtro da API funciona... parece que é por query string.
