---
marp: true
theme: gaia
class: invert
paginate: true
header: '💻 Programando com IA — #fazfadergs'
backgroundColor: #111
style: |
  section {
    font-family: 'Arial', sans-serif;
  }
  h1 {
    color: #4facfe;
  }
  strong {
    color: #00f2fe;
  }
  blockquote {
    border-left: 4px solid #4facfe;
    padding-left: 16px;
    color: #ccc;
    font-style: italic;
  }
---

<!-- _class: lead -->

# 💻 Programando com IA
## Como Desenvolvedores Trabalham Hoje

### Wagner Sabino
📍 FADERGS • Sala 1004 • 10/03 às 19h

🔗 [github.com/SabinoWS/oficinaBabyStepsIA](https://github.com/SabinoWS/oficinaBabyStepsIA)

**#fazfadergs**

---

<!-- _class: lead -->

# 👋 Quem sou eu?

<div style="display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 20px; margin-top: 20px;">
  <div style="width: 120px; height: 120px; border-radius: 50%; background: linear-gradient(135deg, #4facfe, #00f2fe); display: flex; align-items: center; justify-content: center; font-size: 3em;">
    🧑‍💻
  </div>
  <div style="background-color: #1a2e33; padding: 24px 40px; border-radius: 16px; border-left: 6px solid #4facfe; text-align: left; min-width: 500px;">
    <div style="color: #fff; font-size: 1.3em; line-height: 2;">
      💼 &nbsp;<span style="color: #4facfe;">Atuação</span><br>
      🎓 &nbsp;<span style="color: #4facfe;">Formação</span><br>
      ❤️ &nbsp;<span style="color: #4facfe;">O que me apaixona</span>
    </div>
  </div>
</div>

---

<!-- class: default -->

# 📅 Agenda — 📚 Parte 1: Teoria

1. O que é IA? 🤔
2. De Chatbot a Agente 🤖 → 🦾
3. Configurando o Agente 🛠️ *(rules, skills e workflows)*
4. Conceitos: Memória, SDD e MCP 🧠
5. Demo ao vivo 🔥

---

# 📅 Agenda — 🛠️ Parte 2: Prática

6. Projeto 1: Painel Rick and Morty 👽
7. Projeto 2: Pokédex com PokéAPI 🎮
8. Mostra dos resultados 💬
9. Reflexões e mais conversas 🧠

---

<!-- _class: lead -->

# 📚 PARTE 1
## Teoria & Conceitos

---

# 🤔 Pra começar

## Onde e quando vocês já utilizaram IA?

<div style="background-color: #1a2e33; padding: 30px; border-radius: 16px; margin-top: 20px; border-left: 6px solid #4facfe; box-shadow: 0 4px 6px rgba(0,0,0,0.3);">
  <div style="font-size: 1.3em; color: #fff;">
    💬 ChatGPT? Gemini? Copilot? Medo? Empolgação?
  </div>
  <div style="margin-top: 12px; color: #aaa;">
    Não tem resposta errada! Ainda ninguém sabe ao certo o futuro da IA.
  </div>
</div>

---

# 🧠 IA no dia a dia

Vocês já usam IA **sem perceber**:

- 📱 **Corretor do celular** prevê sua próxima palavra
- 🎵 **Spotify** sugere músicas que você vai gostar
- 📸 **Instagram** decide o que aparece no feed
- 🗺️ **Google Maps** calcula a rota mais rápida
- 🔍 **Google** entende o que você quer mesmo digitando errado

**IA não é mágica.** É matemática + dados + padrões.

---

<!-- _class: lead -->

# De Chatbot a Agente
## A grande diferença

---

# 💬 O que é um Chatbot?

- Você pergunta, ele responde
- **Esquece tudo** na próxima conversa
- Só texto, sem ações reais
- Não lê arquivos, não roda nada

> Exemplo: ChatGPT no navegador, Gemini...

---

# 🦾 O que é um Agente de IA?

- **Lê** seus arquivos e entende o projeto
- **Escreve** código diretamente no editor
- **Roda** comandos no terminal
- **Lembra** do contexto enquanto trabalha

> Exemplo: GitHub Copilot no VS Code

---

# 🚗 Uma analogia simples

<div style="background-color: #2a2a2a; padding: 20px; border-radius: 12px; margin-bottom: 20px; border-left: 6px solid #ff5f5f;">
  <div style="color: #ff5f5f; font-weight: bold; margin-bottom: 8px;">💬 Chatbot = GPS de voz</div>
  <div style="color: #aaa;">
    Só responde quando você pergunta.<br>
    "Vire à direita em 200 metros."
  </div>
</div>

<div style="background-color: #1a2e33; padding: 20px; border-radius: 12px; border-left: 6px solid #4facfe;">
  <div style="color: #4facfe; font-weight: bold; margin-bottom: 8px;">🦾 Agente = Copiloto</div>
  <div style="color: #fff;">
    Olha o mapa, sugere rotas, já liga o pisca pra você.<br>
    <strong>"Tem um acidente na frente, já mudei a rota."</strong>
  </div>
</div>

---

<!-- _class: lead -->

# Configurando o Agente
## Rules, Skills & Workflows

---

# 🧠 Por que configurar o Agente?

**1. Eficiência de Contexto**
Em vez de repetir todo dia o que você quer, isso vira uma **configuração permanente**.

**2. Memória de Longo Prazo**
O agente "lembrará" como operar no seu projeto via **Skills**, sem você colar documentação a cada prompt.

**3. Comandos Naturais**
Transforme prompts gigantes em pedidos simples.

---

# 📂 A Estrutura de um Agente

A "bancada" do Agente é organizada em pastas:

```
.agent/
 ├── rules/       # 🧠 Contexto e Diretrizes (O que saber?)
 ├── skills/      # 🛠️ Ferramentas (Como fazer?)
 └── workflows/   # 📋 Processos (O que fazer passo-a-passo?)
```

Se não está aqui, o agente **não sabe**.

---

# 📏 Rules (Regras)

**O que são?**
Diretrizes que governam o comportamento do agente. O "contexto sistêmico" que garante segurança e estilo.

**Para que servem?**
Para evitar que o agente tome ações indesejadas e forçar padrões de qualidade.

> **Exemplo:**
> `"Nunca altere arquivos de configuração (.env, docker-compose) sem pedir confirmação ao usuário."`

---

# 🛠️ Skills (Habilidades)

**O que são?**
Pacotes de conhecimento operacional. Uma Skill ensina ao agente **como** usar uma ferramenta ou executar um procedimento.

**Para que servem?**
Para expandir o "canivete suíço" do agente. Em vez de apenas gerar texto, ele se especializa.

> **Exemplo — Skill: `git-ops`**
> Ensina o agente a fazer `git checkout -b`, `git add`, `git commit` seguindo o padrão do time.

---

# 🔀 Workflows (Fluxos)

**O que são?**
Sequências orquestradas de tarefas. Um "roteiro" passo-a-passo que o agente segue.

**Para que servem?**
Para padronizar processos repetitivos e propensos a erro.

> **Exemplo — Workflow: `deploy-production`**
> 1. Identificar a tag de release e preencher parâmetros de build.
> 2. Submeter deploy e notificar o time.

---

<div style="background-color: #2a2a2a; padding: 20px; border-radius: 12px; margin-bottom: 20px; border-left: 6px solid #ff5f5f; box-shadow: 0 4px 6px rgba(0,0,0,0.3);">
  <div style="color: #ff5f5f; font-weight: bold; font-size: 1.1em; margin-bottom: 8px;">❌ Antes (Verboso)</div>
  <div style="color: #aaa; font-style: italic;">
    "Por favor, faça o deploy, lembrando de rodar testes, verificar a tag, confirmar no chat, commit no padrão tal e depois push ..."
  </div>
</div>

<div style="background-color: #1a2e33; padding: 20px; border-radius: 12px; border-left: 6px solid #4facfe; box-shadow: 0 4px 6px rgba(0,0,0,0.3);">
  <div style="color: #4facfe; font-weight: bold; font-size: 1.1em; margin-bottom: 8px;">✅ Depois (Natural)</div>
  <div style="color: #fff; font-size: 1.4em; font-weight: bold;">
    "Faça o deploy."
  </div>
</div>

---

<!-- _class: lead -->

# Conceitos e Metodologias

---

# 🧠 Memória por Arquivo

**A filosofia:**
O chat é efêmero, volátil e não confiável para guardar decisões.

- **Chat**: Apenas para pedir, ajustar e comandar.
- **Arquivo (.md)**: A única fonte de verdade e persistência.

Se você não escreveu no arquivo, para a IA, **não existe**.

🔗 [github.com/OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files)

> *Mantenha a documentação viva e o contexto salvo.*

---

# 📜 Spec Driven Development (SDD)

**O problema do Chat:**
Conversar "de boca" com a IA gera loops de erro e esquecimento de contexto.

**A solução SDD:**
1. Escreva o que você quer num arquivo Markdown (Spec).
2. A IA lê a Spec.
3. A IA implementa baseado na Spec (não na memória).

> "O Markdown é a API de comunicação entre Humano e Agente."

---

# 📝 Exemplo Prático de SDD

**1. O Humano escreve a Spec (`feature-login.md`):**

```markdown
# Funcionalidade de Login
- O usuário deve logar com email e senha.
- Se errar 3 vezes, bloquear por 15min.
- Retornar erro 401 se credenciais inválidas.
```

**2. O Agente lê e Implementa:**
O agente gera o código **exatamente** como definido no Markdown, sem inventar moda.

---

# 🔌 MCP: Model Context Protocol

**Como conectar a IA ao mundo real?**
O **MCP** é um padrão aberto que permite ao Agente atuar fora da IDE.

- **Ler tickets no Jira** 🎫
- **Consultar documentação no Confluence** 📚
- **Acessar Banco de Dados** 🗄️
- **Pesquisar na Web** 🌐

É a ponte segura entre o "cérebro" da IA e os dados do mundo real.

---

# 🛠️ A Ferramenta de Hoje

**VS Code** = O editor de código (onde você escreve)
**GitHub Copilot** = O agente de IA que vive dentro do editor

<div style="background-color: #1a2e33; padding: 20px; border-radius: 12px; margin-top: 20px; border-left: 6px solid #4facfe;">
  <div style="color: #4facfe; font-weight: bold; margin-bottom: 8px;">✨ O que o Copilot faz?</div>
  <ul style="color: #fff;">
    <li>Completa seu código automaticamente</li>
    <li>Responde perguntas no chat</li>
    <li>Cria arquivos inteiros</li>
    <li>Explica código que você não entende</li>
  </ul>
</div>

---

<!-- _class: lead -->

# 🔥 Demo ao Vivo
## IA programando em tempo real!

---

# 📝 O segredo: **Pedir bem**

<div style="background-color: #2a2a2a; padding: 20px; border-radius: 12px; margin-bottom: 20px; border-left: 6px solid #ff5f5f;">
  <div style="color: #ff5f5f; font-weight: bold; font-size: 1.1em; margin-bottom: 8px;">❌ Pedido Vago</div>
  <div style="color: #aaa; font-style: italic;">
    "Faz uma página web pra mim"
  </div>
</div>

<div style="background-color: #1a2e33; padding: 20px; border-radius: 12px; border-left: 6px solid #4facfe;">
  <div style="color: #4facfe; font-weight: bold; font-size: 1.1em; margin-bottom: 8px;">✅ Pedido Claro</div>
  <div style="color: #fff; font-size: 1.1em;">
    "Crie uma página web pessoal com tema escuro, com meu nome, uma bio curta, meus hobbies em cards, e animações suaves."
  </div>
</div>

> **Quanto melhor o pedido, melhor o resultado!**

---

<!-- _class: lead -->

# 🔄 Fluxo de Trabalho Real
## Como equipes de verdade desenvolvem software

---

# 🔄 O Pipeline Completo

Software não nasce de um pedido direto. Passa por **etapas e responsáveis**:

**🏢 Negócio** → **🕵️ Analista** → **🏛️ Arquiteto** → **⚙️ Engenheiro** → **💻 Dev**

Cada papel tem:
- 📥 Uma **entrada** (o que recebe)
- 🧠 Um **trabalho** (o que faz)
- 📤 Uma **saída** (o que entrega para o próximo)

---

# 🔄 Exemplo Prático

Imagine que a faculdade pede um **sistema de matrícula**:

| Quem | O que faz | Entrega |
|---|---|---|
| 🕵️ **Analista** | Entende o pedido | Requisitos de negócio |
| ⚙️ **Engenheiro** | Planeja a construção | Tasks técnicas |
| 💻 **Dev** | Codifica a solução | Código (commits/PRs) |

---

# 🤖 Onde a IA entra nesse fluxo?

A IA bem configurada pode ajudar em **cada etapa**:

- 🕵️ **Analista** → IA organiza anotações e gera requisitos estruturados
- ⚙️ **Engenheiro** → IA analisa o código e sugere tasks com estimativa de esforço
- 💻 **Desenvolvedor** → IA implementa código seguindo as tasks

<div style="background-color: #1a2e33; padding: 15px; border-radius: 12px; margin-top: 15px; border-left: 6px solid #4facfe;">
  <div style="color: #fff;">
    💡 A IA <strong>propõe</strong>, o humano <strong>aprova</strong>.<br>
    Quanto melhor o contexto (Rules, Skills, Specs), melhor o resultado.
  </div>
</div>

---

<!-- _class: lead -->

# 🛠️ PARTE 2
## Prática — Mão na Massa!

---

<!-- _class: lead -->

# 👽 Projeto 1
## Painel Rick and Morty

---

# 👽 Rick and Morty — O Desafio

Criar um **painel de personagens** usando a [Rick and Morty API](https://rickandmortyapi.com/)!

**O que a página deve ter:**
- 📋 Lista de personagens com foto e nome
- 🟢🔴 Status: Alive, Dead ou Unknown
- 🌍 Localização e espécie
- 🔍 Filtro por nome ou status

**API gratuita, sem cadastro:** `https://rickandmortyapi.com/api/character`

---

# 👽 Rick and Morty — Passo a passo

**Rodada 1** — Peçam para a IA:
```
Crie uma página web que lista os personagens de
Rick and Morty usando a API rickandmortyapi.com.
Mostre foto, nome e status de cada um.
```

**Rodada 2** — Melhorem:
```
Adicione cards estilizados com tema escuro.
O status "Alive" deve ter um ícone verde,
"Dead" vermelho e "Unknown" cinza.
Adicione paginação.
```

**Rodada 3** — Criem um `spec.md` com todos os requisitos!

---

# 👽 Rick and Morty — Dicas

- **Paginação**: A API retorna 20 por página com `?page=2`
- **Filtros**: `?name=rick&status=alive`
- **Imagens**: Já vem no campo `image` do JSON
- **Desafio bônus**: Adicionar página de detalhes ao clicar

> Combinem com o que aprenderam sobre **pedir bem** e **Spec por arquivo**!

---

<!-- _class: lead -->

# 🎮 Projeto 2
## Pokédex com PokéAPI

---

# 🎮 Pokédex — O Desafio

Criar uma **Pokédex interativa** que consulta a [PokéAPI](https://pokeapi.co/)!

**O que a página deve ter:**
- 🔍 Campo de busca por nome ou número
- 🖼️ Imagem do Pokémon
- 📊 Stats (HP, Ataque, Defesa...)
- 🎨 Cores baseadas no tipo (fogo = vermelho, água = azul...)

**API gratuita, sem cadastro:** `https://pokeapi.co/api/v2/pokemon/{nome}`

---

# 🎮 Pokédex — Passo a passo

**Rodada 1** — Peçam para a IA:
```
Crie uma Pokédex web que busca pokémons na PokéAPI.
Mostre a imagem, nome, número e tipos.
```

**Rodada 2** — Melhorem:
```
Adicione as stats do pokémon em barras de progresso.
Use cores diferentes para cada tipo.
Adicione tema escuro.
```

**Rodada 3** — Criem um arquivo `spec.md` com os requisitos!

---

# 🎮 Pokédex — Dicas

- **Endpoint de imagem**: A PokéAPI retorna sprites no JSON
- **Tipos com cores**: Fire 🔴, Water 🔵, Grass 🟢, Electric 🟡
- **Testem com**: Pikachu, Charizard, Bulbasaur, Mewtwo
- **Desafio bônus**: Listar os primeiros 20 pokémons automaticamente

> A API é gratuita e não precisa de cadastro!

---

<!-- _class: lead -->

# 💬 Mostra dos Resultados
## Quem quer mostrar o que fez?

---

# 🤔 O que muda com isso?

<div style="background-color: #1a2e33; padding: 25px; border-radius: 16px; border-left: 6px solid #4facfe;">
  <div style="color: #fff; font-size: 1.1em; line-height: 1.8;">
    ✅ Vocês criaram algo que <strong>levaria horas</strong> para aprender sozinhos<br><br>
    ✅ A IA <strong>não substitui</strong> vocês — mas quem sabe usar IA terá <strong>vantagem</strong><br><br>
    ✅ O segredo não é saber programar tudo — é saber <strong>PEDIR</strong> bem<br><br>
    ✅ Errar faz parte — a IA erra, você corrige, e <strong>juntos</strong> chegam lá
  </div>
</div>

---

# 📚 Continue Aprendendo

| Recurso | Link |
|---|---|
| 🛠️ VS Code | [code.visualstudio.com](https://code.visualstudio.com) |
| 🤖 GitHub Copilot | [github.com/features/copilot](https://github.com/features/copilot) |
| 🎓 GitHub Education | [education.github.com](https://education.github.com) |
| 📝 Markdown | [markdownguide.org](https://www.markdownguide.org) |

<div style="background-color: #1a2e33; padding: 15px; border-radius: 12px; margin-top: 15px; border-left: 6px solid #4facfe;">
  <div style="color: #4facfe; font-weight: bold;">💡 Dica!</div>
  <div style="color: #fff;">
    Com o email da faculdade, vocês podem pedir o <strong>GitHub Student Pack</strong> — inclui Copilot <strong>grátis</strong>!
  </div>
</div>

---

<!-- _class: lead -->

# 🙏 Obrigado!

### Wagner Sabino

💬 Perguntas? Dúvidas? Ideias?

**#fazfadergs** • FADERGS

> _"O melhor jeito de aprender IA é usando IA."_
