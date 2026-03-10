---
name: Criador de Slides Marp
description: Guia especialista para criar apresentações de alta qualidade e visualmente agradáveis usando Marp (Markdown).
---

# Skill: Criador de Slides Marp

Esta skill ajuda você a criar apresentações profissionais e bonitas usando Marp.

## 🚀 Início Rápido

Para ativar o Marp em um arquivo markdown, adicione este frontmatter logo no início:

```markdown
---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
---
```

## 🎨 Conceitos Principais

### 1. Temas
O Marp vem com 3 temas integrados:
- `default`: Fundo branco limpo. Bom para documentação.
- `gaia`: Focado em slides, colorido. Ótimo para palestras. (Suporta `class: lead` para slides de título).
- `uncover`: Minimalista, conteúdo centralizado. Bom para pontos rápidos e texto grande.

### 2. Diretivas
- `paginate: true` — Adiciona números de página.
- `header: 'Meu Título'` — Adiciona um cabeçalho em todos os slides.
- `footer: 'Confidencial'` — Adiciona um rodapé.
- `backgroundColor: #f0f0f0` — Define a cor de fundo do slide.
- `color: #333` — Define a cor do texto.

### 3. Imagens de Fundo
- `![bg](image.jpg)` — Fundo para o slide.
- `![bg cover](image.jpg)` — Cobre o slide inteiro (padrão).
- `![bg right](image.jpg)` — Divide a tela, imagem à direita (50%).
- `![bg left:33%](image.jpg)` — Divide a tela, imagem à esquerda (33%).

## 💅 Boas Práticas Visuais

1. **Hierarquia Visual**: Use H1 para títulos principais (um por slide), H2 para cabeçalhos de seção.
2. **Menos é Mais**: Tópicos devem ser concisos. Evite paredes de texto.
3. **Contraste**: Garanta que o texto seja legível contra os fundos. Use `class: invert` no tema Gaia para slides escuros.
4. **Blocos de Código**: O Marp lida com destaque de sintaxe automaticamente. Ótimo para palestras técnicas.

## 🛠️ Modelos Comuns

### Slide de Título (Capa)
```markdown
---
marp: true
theme: gaia
_class: lead
backgroundColor: #fff
---

# Título da Apresentação
## Subtítulo vai aqui
### Nome do Autor
```

### Layout com Imagem à Direita
```markdown
---
# Nossa Estratégia

- **Ponto 1**: Descrição.
- **Ponto 2**: Descrição.
- **Ponto 3**: Descrição.

![bg right:40%](https://picsum.photos/800/600)
```

### Citação / Frase de Impacto
```markdown
<!-- _class: lead -->

> "A única maneira de fazer um ótimo trabalho é amar o que você faz."
>
> — Steve Jobs
```
