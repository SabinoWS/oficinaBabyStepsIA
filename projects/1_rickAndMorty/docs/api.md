# 📖 Documentação da Rick and Morty API

> **URL Base:** `https://rickandmortyapi.com/api/`
> **Autenticação:** Não necessária ✅
> **Métodos:** REST (GET) e GraphQL

---

## 📌 O que é a Rick and Morty API?

A **Rick and Morty API** é uma API REST e GraphQL gratuita com dados completos da série animada Rick and Morty. Não é necessário cadastro nem token de acesso.

Ela reúne **826 personagens**, **126 localizações** e **51 episódios** — todos disponíveis gratuitamente.

---

## 🚀 Endpoints Principais

### 1. Listar Personagens (com paginação)

```
GET https://rickandmortyapi.com/api/character
```

A API pagina automaticamente: **20 personagens por página**.

**Resposta:**
```json
{
  "info": {
    "count": 826,
    "pages": 42,
    "next": "https://rickandmortyapi.com/api/character/?page=2",
    "prev": null
  },
  "results": [
    {
      "id": 1,
      "name": "Rick Sanchez",
      "status": "Alive",
      "species": "Human",
      "type": "",
      "gender": "Male",
      "origin": {
        "name": "Earth (C-137)",
        "url": "https://rickandmortyapi.com/api/location/1"
      },
      "location": {
        "name": "Citadel of Ricks",
        "url": "https://rickandmortyapi.com/api/location/3"
      },
      "image": "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
      "episode": [
        "https://rickandmortyapi.com/api/episode/1",
        "https://rickandmortyapi.com/api/episode/2"
      ],
      "url": "https://rickandmortyapi.com/api/character/1",
      "created": "2017-11-04T18:48:46.250Z"
    }
  ]
}
```

---

### 2. Navegar entre páginas

```
GET https://rickandmortyapi.com/api/character/?page=2
GET https://rickandmortyapi.com/api/character/?page=19
```

Use o campo `info.next` e `info.prev` da resposta para navegar entre as páginas dinamicamente.

---

### 3. Buscar um personagem específico por ID

```
GET https://rickandmortyapi.com/api/character/{id}
```

**Exemplos:**
```
https://rickandmortyapi.com/api/character/1    → Rick Sanchez
https://rickandmortyapi.com/api/character/2    → Morty Smith
https://rickandmortyapi.com/api/character/361  → Toxic Rick
```

---

### 4. Filtrar personagens

```
GET https://rickandmortyapi.com/api/character/?{filtro}={valor}
```

Você pode combinar múltiplos filtros com `&`:

| Filtro | Valores possíveis |
|---|---|
| `name` | qualquer texto |
| `status` | `alive`, `dead`, `unknown` |
| `species` | `Human`, `Alien`, `Humanoid`, etc. |
| `gender` | `female`, `male`, `genderless`, `unknown` |

**Exemplos:**
```
# Todos os Ricks vivos
https://rickandmortyapi.com/api/character/?name=rick&status=alive

# Todos os humanos
https://rickandmortyapi.com/api/character/?species=Human

# Mortas do gênero feminino
https://rickandmortyapi.com/api/character/?status=dead&gender=female
```

---

## 📋 Campos do Personagem (Character)

| Campo | Tipo | Descrição |
|---|---|---|
| `id` | number | ID único do personagem |
| `name` | string | Nome completo |
| `status` | string | `Alive`, `Dead` ou `unknown` |
| `species` | string | Espécie (Human, Alien...) |
| `type` | string | Sub-tipo (pode ser vazio) |
| `gender` | string | `Male`, `Female`, `Genderless`, `unknown` |
| `origin.name` | string | Local de origem |
| `location.name` | string | Localização atual |
| `image` | string | URL da imagem (JPEG) |
| `episode` | array | Lista de URLs dos episódios em que aparece |

---

## 🎨 Status com Cores Sugeridas

Use estas cores para indicar o status do personagem:

| Status | Ícone | Cor sugerida |
|---|---|---|
| Alive | 🟢 | `#00b341` |
| Dead | 🔴 | `#e03c3c` |
| unknown | ⚫ | `#9e9e9e` |

---

## 💻 Exemplo de Uso em JavaScript

```javascript
// Listar personagens da página 1
async function listarPersonagens(pagina = 1) {
  const url = `https://rickandmortyapi.com/api/character/?page=${pagina}`;
  const response = await fetch(url);
  const data = await response.json();

  return {
    info: data.info,          // paginação
    personagens: data.results // array de personagens
  };
}

// Filtrar por nome e status
async function filtrarPersonagens(nome = '', status = '') {
  const params = new URLSearchParams();
  if (nome) params.append('name', nome);
  if (status) params.append('status', status);

  const url = `https://rickandmortyapi.com/api/character/?${params}`;
  const response = await fetch(url);

  if (!response.ok) return { results: [] };

  const data = await response.json();
  return data;
}

// Uso:
listarPersonagens(1).then(d => console.log(d.personagens));
filtrarPersonagens('rick', 'alive').then(d => console.log(d.results));
```

---

## 🧪 Personagens para testar

| Nome | ID | Status |
|---|---|---|
| Rick Sanchez | 1 | Alive |
| Morty Smith | 2 | Alive |
| Summer Smith | 3 | Alive |
| Beth Smith | 4 | Alive |
| Jerry Smith | 5 | Alive |
| Abadango Cluster Princess | 6 | Alive |
| Toxic Rick | 361 | Dead |
| Evil Morty | 116 | Alive |

---

## 🔗 Links Úteis

- **Documentação oficial:** https://rickandmortyapi.com/documentation
- **API base:** https://rickandmortyapi.com/api/
- **Status da API:** https://status.rickandmortyapi.com
