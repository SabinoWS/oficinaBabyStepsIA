# 🎓 Oficina: Baby Steps com IA — Plano para Faculdade

> **Público-alvo:** Calouros de faculdade (iniciantes em programação/tecnologia)
> **Duração sugerida:** 2h a 3h (flexível, ajustar conforme energia do grupo)
> **Formato:** Mão-na-massa (hands-on), conversacional e com demonstrações ao vivo
> **Ferramenta principal:** VS Code + GitHub Copilot | **Fallback:** Cursor (versão gratuita)

---

## 📌 Contexto & Motivação

Você já conduziu um **Dojo interno** para o time de tecnologia da empresa, cobrindo temas avançados como Rules, Skills, Workflows, SDD (Spec Driven Development), MCP (Model Context Protocol) e o Canonical Cycle — tudo voltado para profissionais que já trabalham com o Antigravity do Google.

Agora, o desafio é **traduzir essa experiência para calouros** que, potencialmente:
- Estão começando a programar (ou ainda nem começaram)
- Nunca usaram uma IDE com IA integrada
- Conhecem IA apenas como "ChatGPT" no navegador
- Não sabem o que é terminal, git, ou Markdown

A oficina precisa ser **inspiradora, acessível e prática**.

---

## 🎯 Objetivos da Oficina

1. **Desmistificar a IA** — Mostrar que IA não é "mágica" nem "vai roubar o emprego", é uma **ferramenta de trabalho**
2. **Apresentar o conceito de Agente de IA** — Sair do "chatbot" para o "parceiro de trabalho"
3. **Dar uma experiência prática** — Os alunos devem sair tendo feito algo real com ajuda de IA
4. **Plantar a semente da engenharia de prompt** — A ideia de que como você pede é tão importante quanto o que pede
5. **Mostrar o futuro do trabalho** — Como profissionais de tecnologia já trabalham com IA no dia a dia

---

## 🧩 Estrutura Proposta (3 blocos)

### 🟢 Bloco 1 — Conversa & Conceitos (30-40 min)
> Objetivo: Aquecer, criar conexão e nivelar o entendimento

#### 1.1 Abertura: "O que vocês acham que IA é?"
- Abrir com pergunta aberta
- Deixar os alunos falarem (mesmo respostas "erradas" são valiosas)
- Coletar percepções: filme, chatgpt, robôs, medo, empolgação

#### 1.2 De Chatbot a Agente
- **Chatbot**: Você pergunta, ele responde. Ele esquece tudo na próxima conversa.
- **Agente de IA**: Ele **lê arquivos**, **roda comandos**, **edita código**, **lembra do contexto** e **toma ações**.
- Analogia: _"Chatbot é como um GPS de voz que só responde quando você pergunta. Agente é como um copiloto que olha o mapa, sugere rotas e já liga o pisca pra você."_

#### 1.3 Demo ao vivo rápida (5 min)
- Abrir o **VS Code com GitHub Copilot** (ferramenta que os alunos vão usar)
- Mostrar uma interação real: pedir para o agente criar um arquivo, editar algo, rodar um comando
- **Efeito WOW**: Os calouros veem a IA escrevendo código em tempo real no editor

#### 1.4 Os 3 superpoderes do Agente
Simplificar a estrutura do dojo em 3 conceitos palpáveis:

| Superpoder | No Dojo (avançado) | Na Oficina (simplificado) |
|---|---|---|
| 🧠 **Memória** | Rules + arquivos .md | "Se não tá escrito, a IA não sabe" |
| 🛠️ **Habilidades** | Skills | "Ensinar a IA *como* fazer algo" |
| 📋 **Receitas** | Workflows | "Passo-a-passo que a IA segue" |

---

### 🟡 Bloco 2 — Mão na Massa! (60-80 min)
> Objetivo: Fazer os alunos criarem algo real com ajuda de IA

#### Opção A: **"Crie sua página pessoal com IA"** ⭐ (Recomendada)

**Por que?** Todo mundo gosta de falar de si. Gera engajamento natural.

**O que fazer:**
1. Cada aluno (ou dupla) abre o editor com IA
2. O desafio: **"Peça para a IA criar uma página web sobre você"**
3. Etapas guiadas:
   - **Rodada 1**: Pedir a página de qualquer jeito e ver o resultado (provável que seja OK mas genérica)
   - **Rodada 2**: Aprender a dar instruções melhores — adicionar detalhes, estilo, cores
   - **Rodada 3**: Criar um arquivo `.md` com suas informações e pedir para a IA ler esse arquivo e usar como base
   - **(Opcional) Rodada 4**: Pedir para a IA adicionar animações, tema escuro, efeitos visuais

**Conceitos que entram organicamente:**
- Engenharia de Prompt (pedir melhor = resultado melhor)
- Memória por Arquivo (Spec/SDD simplificado — a IA lê o .md em vez de depender do chat)
- Iteração (não precisa acertar de primeira)

#### Opção B: **"Resolva um mistério com IA"** 🔎

**Por que?** Gamificação. Bom para turmas mais lúdicas.

**O que fazer:**
1. Você prepara um "caso" com pistas em vários arquivos .txt numa pasta
2. Os alunos pedem para a IA ler os arquivos e ajudar a resolver o mistério
3. Quem "resolver" primeiro ganha um prêmio

**Conceitos que entram:**
- IA lendo arquivos (ferramenta, não chatbot)
- Dar contexto (as pistas) faz a diferença
- Trabalho iterativo

#### Opção C: **"Jogo da Velha com IA"** 🎮

**Por que?** Clássico, visual, e demonstra lógica de programação.

**O que fazer:**
1. Pedir para a IA criar um Jogo da Velha jogável no navegador
2. Customizar: cores, nomes dos jogadores, placar
3. Desafio extra: pedir para a IA adicionar um "jogador IA" (bot)

**Conceitos que entram:**
- IA criando algo funcional (código que roda!)
- Especificar requisitos (features)
- Iterar e melhorar

---

### 🔵 Bloco 3 — Reflexão & Fechamento (20-30 min)
> Objetivo: Consolidar aprendizado e inspirar

#### 3.1 Mostra dos Resultados (10 min)
- Quem quiser, mostra o que fez
- Celebrar todas as tentativas (mesmo as que "deram errado" — é aprendizado)

#### 3.2 "O que muda com isso?" (10 min)
- Reflexão coletiva:
  - _"Vocês acabaram de criar algo que levaria horas/dias para aprender sozinhos"_
  - _"A IA não substitui vocês — mas quem sabe usar IA vai ter vantagem"_
  - _"O segredo não é saber programar tudo, é saber PEDIR bem"_

#### 3.3 Ponte para o Futuro (5 min)
- Mostrar brevemente o que profissionais fazem (tela do dojo, workflow real)
- Mensagem: _"O que vocês fizeram hoje é o primeiro passo. Daqui a pouco, agentes de IA vão ser tão comuns quanto planilhas."_
- Deixar links/recursos para quem quiser continuar explorando

---

## 💡 Ideias Extras & Dicas

### 🎨 Projetos Alternativos (se sobrar tempo ou para workshops maiores)
- **Quiz interativo**: IA cria um quiz sobre um tema que os alunos escolhem
- **Gerador de memes**: Página que gera frases engraçadas automaticamente
- **Portfólio de turma**: Cada aluno faz uma seção e junta tudo numa página só
- **Chatbot temático**: Criar um personagem que responde perguntas (ex: "Harry Potter responde suas dúvidas de faculdade")

### 🛠️ Setup Técnico
- **Editor principal**: VS Code + extensão GitHub Copilot
- **Fallback**: Cursor (versão gratuita) — útil se houver problema com licenças do Copilot ou se quiser mostrar uma experiência de chat + agente mais integrada
- **Pré-requisito dos alunos**: Nenhum! (só precisam de um computador)
- **Contas necessárias**: Conta GitHub (gratuita) com acesso ao Copilot (verificar se a faculdade tem GitHub Education — dá Copilot grátis para alunos!)
- **Preparar antes**: 
  - Máquinas com VS Code instalado + extensão Copilot configurada
  - Uma pasta com arquivos de exemplo para cada exercício
  - Slides simples (pode usar Marp como no dojo!)
  - Wi-Fi funcionando (essencial!)

### 📢 Dicas de Facilitação
- **Não assuma conhecimento**: Explique o que é terminal, o que é HTML, o que é um arquivo .md
- **Use analogias do dia a dia**: A IA é como um estagiário muito inteligente mas que precisa de instruções claras
- **Erros são Features**: Quando der errado ao vivo, use como momento de ensino ("Viram? A IA errou porque eu não expliquei direito!")
- **Mantenha energia alta**: Intercale demo e prática, nunca fique mais de 15 min só falando
- **Duplas/trios**: Se tiver mais gente que máquinas, incentive trabalho em grupo (pair programming com IA!)

### 🧊 Icebreakers Temáticos
- _"Qual filme/série com IA vocês já viram?"_
- _"Se vocês pudessem ter um robô assistente, o que ele faria?"_
- _"Quantos de vocês já usaram ChatGPT? Para quê?"_

---

## 🗂️ Materiais a Preparar

| Material | Descrição | Prioridade |
|---|---|---|
| Slides introdutórios | 10-15 slides simples e visuais (Marp/Google Slides) | 🔴 Alta |
| Pasta de exemplo | Arquivos .md e .txt para os exercícios | 🔴 Alta |
| Guia do aluno | 1 página com passo-a-passo do exercício | 🟡 Média |
| README do repositório | Explicação do projeto para quem quiser revisitar | 🟡 Média |
| Formulário de feedback | Google Forms simples para coletar impressões | 🟢 Baixa |
| Lista de recursos | Links para quem quiser continuar aprendendo depois | 🟢 Baixa |

---

## 🔗 Conexão com o Dojo Original

O dojo interno abordou conceitos profundos e profissionais. Aqui está como **simplificar** cada um para a oficina:

| Conceito do Dojo | Versão Simplificada para Calouros |
|---|---|
| **Rules** | "Diga para a IA o que ela NÃO pode fazer" (ex: "não delete meus arquivos") |
| **Skills** | "Ensine a IA a fazer algo específico" (ex: descreva como é seu estilo) |
| **Workflows** | "Crie uma receita passo-a-passo" (ex: 1. leia meu arquivo, 2. crie a página, 3. adicione fotos) |
| **SDD** | "Escreva o que quer num arquivo. A IA lê e faz." |
| **Memória por Arquivo** | "Chat = conversa que some. Arquivo = lembrança que fica." |
| **MCP** | ❌ Pular na oficina (muito avançado) |
| **Canonical Cycle** | ❌ Pular na oficina (muito avançado). Apenas mencionar a ideia: "IA propõe, humano aprova" |

---

## 📋 Checklist Pré-Oficina

- [ ] Definir data, horário e local com a faculdade
- [ ] Confirmar quantidade de alunos e máquinas disponíveis
- [ ] Instalar VS Code + extensão Copilot nas máquinas (ou confirmar que alunos trazem notebooks)
- [ ] Garantir contas GitHub com Copilot ativo (verificar GitHub Education)
- [ ] Ter Cursor instalado como fallback em pelo menos algumas máquinas
- [ ] Preparar slides introdutórios
- [ ] Criar pasta de exemplo com exercícios
- [ ] Testar que tudo funciona (Wi-Fi, Copilot logado, extensões ativas)
- [ ] Preparar guia do aluno impresso ou digital
- [ ] Definir qual exercício principal usar (A, B ou C)
- [ ] Preparar um "plano B" caso a internet caia (screenshots de demos, exercício offline)

---

## 🚀 Próximos Passos

1. **Escolher o exercício principal** (recomendo Opção A — Página Pessoal)
2. **Montar os slides** (posso ajudar a criar com Marp!)
3. **Preparar a pasta de exercícios** com templates
4. **Fazer um dry-run** completo sozinho (cronometrar!)
5. **Iterar** com base no feedback do dry-run

---

> 💬 _"O melhor jeito de aprender IA é usando IA. E o melhor jeito de ensinar IA é fazendo as pessoas se surpreenderem com o que conseguem criar."_
