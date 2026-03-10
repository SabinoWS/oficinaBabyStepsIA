# 💻 Programando com IA: Como Desenvolvedores Trabalham Hoje

> **Oficina introdutória sobre uso de IA no desenvolvimento de software.**
> Conceitos básicos, boas práticas da engenharia de software e como a IA pode auxiliar nesse processo.

📍 **FADERGS** • Sala 1004 • 10/03/2026 às 19h
🎤 **Wagner Sabino**
🏷️ **#fazfadergs**

---

## 🎯 Sobre a Oficina

Esta oficina foi criada para **calouros de faculdade** que estão começando sua jornada na tecnologia. O objetivo é desmistificar a Inteligência Artificial e mostrar, na prática, como desenvolvedores de software já trabalham com IA no dia a dia.

### O que vamos abordar?

1. **O que é IA?** — Saindo do "medo" e da "mágica" para o entendimento prático
2. **De Chatbot a Agente** — A diferença entre um chat passivo e um parceiro de trabalho
3. **Demo ao vivo** — IA programando em tempo real dentro do editor
4. **Mão na massa!** — Os alunos criam sua própria página web pessoal com ajuda de IA
5. **Reflexão** — O que muda no futuro do trabalho?

---

## 🛠️ Ferramentas Utilizadas

| Ferramenta | Uso |
|---|---|
| **VS Code** | Editor de código principal |
| **GitHub Copilot** | Agente de IA integrado ao editor |
| **Cursor** *(fallback)* | Alternativa gratuita com IA integrada |
| **Marp** | Geração dos slides a partir de Markdown |

> 💡 **Dica para alunos**: com o email da faculdade, vocês podem solicitar o [GitHub Student Developer Pack](https://education.github.com), que inclui o **GitHub Copilot gratuitamente**!

---

## 📂 Estrutura do Projeto

```
oficinaBabyStepsIA/
├── README.md                  # Este arquivo
├── slides.md                  # Slides da oficina (Marp)
├── docs/                      # Documentação adicional
├── images/                    # Imagens e assets
├── temporario/                # Arquivos temporários e rascunhos
├── .github/                   # 🐙 Configuração para GitHub Copilot (VS Code)
│   ├── copilot-instructions.md  # Instrução global do Copilot
│   ├── rules/                 # Regras de comportamento (.md)
│   ├── skills/                # Habilidades especializadas (.md)
│   └── iaflows/               # Workflows de IA do Copilot (.md)
├── .agent/                    # ⚡ Configuração para Antigravity (Google Gemini)
│   ├── rules/                 # Regras de comportamento (.md)
│   ├── skills/                # Habilidades especializadas (.md)
│   └── workflows/             # Fluxos de trabalho (.md)
└── .cursor/                   # 🎯 Configuração para Cursor AI
    ├── rules/                 # Regras de comportamento (.mdc)
    ├── skills/                # Habilidades especializadas (.md)
    └── workflows/             # Fluxos de trabalho (.md)
```

---

## 🚀 Como Usar

### Visualizar os Slides
Os slides estão em `temporario/slides.md` no formato [Marp](https://marp.app). Para visualizar:

1. Instale a extensão **Marp for VS Code** no VS Code
2. Abra o arquivo `temporario/slides.md`
3. Use o preview do Marp (ícone no canto superior direito)

Para exportar em PDF:
```bash
npx @marp-team/marp-cli temporario/slides.md --pdf
```

### Configuração dos Agentes de IA

Este projeto está configurado para funcionar com **dois assistentes de IA distintos**, cada um com sua própria pasta de configuração:

---

#### 🐙 `.github/copilot-instructions.md` — GitHub Copilot (VS Code)

Usado pelo **GitHub Copilot** integrado ao VS Code.

| Pasta/Arquivo | Descrição |
|---|---|
| `.github/copilot-instructions.md` | Instrução global: comportamento, idioma, contexto e orquestração |
| `.github/rules/` | Regras de comportamento específicas (`.md`) |
| `.github/skills/` | Habilidades especializadas (`.md`) |
| `.github/iaflows/` | Workflows de IA do Copilot (`.md`) — separado do CI/CD |

---

#### ⚡ `.agent/` — Antigravity (Google Gemini / DeepMind)

Usado pelo **Antigravity**, o assistente de IA da Google integrado via extensão própria.

| Pasta | Descrição |
|---|---|
| `.agent/rules/` | Regras de comportamento em formato `.md` |
| `.agent/skills/` | Habilidades especializadas (ex: analista, arquiteto, revisor) |
| `.agent/workflows/` | Fluxos de trabalho com slash commands (ex: `/canonical-start`) |

---

#### 🎯 `.cursor/` — Cursor AI

Usado pelo **Cursor**, o editor com IA integrada.

| Pasta | Descrição |
|---|---|
| `.cursor/rules/` | Regras de comportamento em formato `.mdc` |
| `.cursor/skills/` | Habilidades especializadas para o Cursor |
| `.cursor/workflows/` | Processos e fluxos de trabalho para o Cursor |

---

> ⚠️ **Importante**: As pastas `.github/`, `.agent/` e `.cursor/` são **separadas intencionalmente**.
> Cada ferramenta tem seu próprio formato, sintaxe e convenções.
> Não misture arquivos entre elas — edite apenas a pasta correspondente ao assistente que está usando.

---

## 📚 Recursos para Continuar Aprendendo

| Recurso | Link |
|---|---|
| VS Code | [code.visualstudio.com](https://code.visualstudio.com) |
| GitHub Copilot | [github.com/features/copilot](https://github.com/features/copilot) |
| GitHub Education | [education.github.com](https://education.github.com) |
| Guia de Markdown | [markdownguide.org](https://www.markdownguide.org) |
| Marp | [marp.app](https://marp.app) |

---

## 👤 Autor

Wagner Sabino
