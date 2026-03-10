# 📖 Documentação da PokéAPI

> **URL Base:** `https://pokeapi.co/api/v2/`
> **Autenticação:** Não necessária ✅
> **Método HTTP:** Apenas `GET` (API somente leitura)

---

## 📌 O que é a PokéAPI?

A **PokéAPI** é uma API REST gratuita e pública com dados completos do universo Pokémon. Não é necessário cadastro nem token de acesso — basta fazer a requisição e usar!

> ⚠️ **Fair Use:** A API é educacional e gratuita. Evite fazer muitas requisições em sequência. Sempre que possível, faça cache dos resultados no navegador (ex: localStorage).

---

## 🚀 Endpoints Principais

### 1. Buscar um Pokémon por nome ou ID

```
GET https://pokeapi.co/api/v2/pokemon/{nome ou id}
```

**Exemplos:**
```
https://pokeapi.co/api/v2/pokemon/pikachu
https://pokeapi.co/api/v2/pokemon/25
https://pokeapi.co/api/v2/pokemon/charizard
```

**Resposta (campos mais úteis para o projeto):**
```json
{
  "id": 25,
  "name": "pikachu",
  "height": 4,
  "weight": 60,
  "base_experience": 112,
  "sprites": {
    "front_default": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png",
    "other": {
      "official-artwork": {
        "front_default": "https://raw.githubusercontent.com/.../official-artwork/25.png"
      }
    }
  },
  "types": [
    {
      "slot": 1,
      "type": { "name": "electric" }
    }
  ],
  "stats": [
    { "base_stat": 35, "stat": { "name": "hp" } },
    { "base_stat": 55, "stat": { "name": "attack" } },
    { "base_stat": 40, "stat": { "name": "defense" } },
    { "base_stat": 50, "stat": { "name": "special-attack" } },
    { "base_stat": 50, "stat": { "name": "special-defense" } },
    { "base_stat": 90, "stat": { "name": "speed" } }
  ],
  "abilities": [
    { "ability": { "name": "static" }, "is_hidden": false }
  ]
}
```

---

### 2. Listar Pokémons (com paginação)

```
GET https://pokeapi.co/api/v2/pokemon?limit=20&offset=0
```

| Parâmetro | Descrição | Padrão |
|---|---|---|
| `limit` | Quantos retornar por página | 20 |
| `offset` | A partir de qual índice começar | 0 |

**Resposta:**
```json
{
  "count": 1302,
  "next": "https://pokeapi.co/api/v2/pokemon?offset=20&limit=20",
  "previous": null,
  "results": [
    { "name": "bulbasaur", "url": "https://pokeapi.co/api/v2/pokemon/1/" },
    { "name": "ivysaur", "url": "https://pokeapi.co/api/v2/pokemon/2/" }
  ]
}
```

> 💡 `results` retorna apenas nome e URL. Para obter detalhes (imagem, stats), é necessário fazer uma segunda requisição para cada URL.

---

## 🎨 Tipos de Pokémon e Cores Sugeridas

Use estas cores para estilizar o card de acordo com o tipo:

| Tipo | Cor (hex) |
|---|---|
| 🔥 fire | `#F08030` |
| 💧 water | `#6890F0` |
| 🌿 grass | `#78C850` |
| ⚡ electric | `#F8D030` |
| 🧊 ice | `#98D8D8` |
| 👊 fighting | `#C03028` |
| ☠️ poison | `#A040A0` |
| 🌍 ground | `#E0C068` |
| 🦅 flying | `#A890F0` |
| 🧠 psychic | `#F85888` |
| 🐛 bug | `#A8B820` |
| 🪨 rock | `#B8A038` |
| 👻 ghost | `#705898` |
| 🐉 dragon | `#7038F8` |
| 🌑 dark | `#705848` |
| ⚙️ steel | `#B8B8D0` |
| 🧚 fairy | `#EE99AC` |
| ⭐ normal | `#A8A878` |

---

## 🖼️ Como pegar a imagem do Pokémon

A forma mais fácil é usar o **artwork oficial** (imagem de alta qualidade):

```javascript
// Usando o ID do Pokémon (ex: 25 = Pikachu)
const imageUrl = `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/${id}.png`;

// Ou diretamente da resposta da API:
const imageUrl = data.sprites.other["official-artwork"].front_default;

// Sprite clássico (pixel art):
const spriteUrl = data.sprites.front_default;
```

---

## 💻 Exemplo de Uso em JavaScript

```javascript
async function buscarPokemon(nomeoOuId) {
  const url = `https://pokeapi.co/api/v2/pokemon/${nomeoOuId}`;

  const response = await fetch(url);

  if (!response.ok) {
    throw new Error('Pokémon não encontrado!');
  }

  const data = await response.json();

  return {
    id: data.id,
    name: data.name,
    image: data.sprites.other["official-artwork"].front_default,
    types: data.types.map(t => t.type.name),
    stats: data.stats.map(s => ({
      name: s.stat.name,
      value: s.base_stat
    }))
  };
}

// Uso:
buscarPokemon('pikachu').then(p => console.log(p));
buscarPokemon(6).then(p => console.log(p)); // charizard
```

---

## 🧪 Pokémons para testar

| Nome | ID |
|---|---|
| Bulbasaur | 1 |
| Charmander | 4 |
| Squirtle | 7 |
| Pikachu | 25 |
| Charizard | 6 |
| Mewtwo | 150 |
| Eevee | 133 |
| Gengar | 94 |

---

## 🔗 Links Úteis

- **Documentação oficial:** https://pokeapi.co/docs/v2
- **API base:** https://pokeapi.co/api/v2/
- **Sprites (GitHub):** https://github.com/PokeAPI/sprites
