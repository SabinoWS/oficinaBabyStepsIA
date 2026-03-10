---
description: Workflow interativo para criar e adicionar slides Marp com revisão e confirmação.
---

# 🎞️ Workflow: Gerador de Slides Interativo

Este workflow guia o agente e o usuário na criação colaborativa de slides, garantindo qualidade e aprovação antes de salvar.

## 1. 🕵️ Análise e Sugestões
1. Leia o arquivo de slides atual (padrão: `slides.md`).
2. Analise o fluxo da apresentação com base no contexto do projeto.
3. **Ação**: Ofereça 3 sugestões de slides relevantes ou melhorias que poderiam ser feitas.

## 2. 🗣️ Coleta de Conteúdo
1. Pergunte ao usuário:
   > "O que você gostaria de adicionar à apresentação agora? Você pode escolher uma das sugestões acima ou propor algo novo."
2. Peça detalhes sobre o conteúdo (tópicos, título, imagem desejada).

## 3. 📍 Definição de Localização
1. Pergunte onde o novo slide deve ser inserido:
   - No início?
   - No final?
   - Depois de qual slide específico?

## 4. ✍️ Geração e Edição
1. Utilize a skill **Criador de Slides Marp** (`.github/skills/marp-slides-creator.md`) para formatar o slide corretamente.
2. Insira o slide no arquivo `slides.md` na posição desejada.
3. **Importante**: Garanta que o slide tenha diretivas visuais adequadas (background, cores, layout).

## 5. ✅ Revisão e Aprovação
1. Mostre o código markdown que foi adicionado.
2. Pergunte explicitamente:
   > "O slide foi adicionado conforme o esperado? Digite 'aprovar' para confirmar ou 'reprovar' para desfazer."

## 6. 🔒 Finalização (Commit ou Revert)
- **SE APROVADO**:
  1. Execute: `git add slides.md`
  2. Confirme: "Alterações adicionadas ao stage do Git. 🚀"

- **SE REPROVADO**:
  1. Desfaça as alterações no arquivo (volte ao estado anterior).
  2. Confirme: "Alterações desfeitas. Vamos tentar novamente? ↺"
