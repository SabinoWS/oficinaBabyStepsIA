---
description: Workflow para submissão segura de código. Mostra identidade, seleciona arquivos, stasha restos, e sincroniza via rebase.
---

# Workflow: Git Submit

Este workflow garante que o código seja enviado com a identidade correta, separação limpa de mudanças e histórico linear.

## 1. Verificação de Identidade
1. Execute `git config user.name` e `git config user.email`.
2. **Informe** ao usuário os valores atuais e pergunte se estão corretos para o contexto (Pessoal vs Trabalho).
3. Pode prosseguir aqui, é apenas informativo.

## 2. Seleção de Mudanças (Stage)
1. Execute `git status` para listar arquivos modificados e não rastreados.
2. Liste as alterações para o usuário.
3. **Pergunte** explicitamente: "Quais arquivos você deseja incluir neste commit?".
4. Com base na resposta:
   - Execute `git add <arquivos>` para os itens escolhidos.
   - Verifique se algo ficou fora do stage.

## 3. Isolamento (Stash)
1. Se houver arquivos modificados que **não** foram adicionados ao stage:
   - Execute `git stash --keep-index -u`.
   - Informe ao usuário: "As alterações não selecionadas foram guardadas temporariamente (stash)."

## 4. Commit
1. Gere uma mensagem de commit baseada nas alterações em stage, seguindo Conventional Commits.
   - **IMPORTANTE**: Não inclua paths completos. Use apenas nomes de arquivos ou descrições funcionais.
   - **IDIOMA**: A mensagem deve estar sempre em **Português (pt-BR)**.
2. **Apresente** a mensagem sugerida e pergunte: "Posso commitar com esta mensagem? (Responda 'Sim' ou forneça uma nova mensagem)".
3. Se aprovado, execute `git commit -m "Sua Mensagem"`.

## 5. Sincronização (Pull & Push)
1. Identifique a branch atual com `git branch --show-current`.
2. Execute `git pull --rebase origin <branch_atual>`.
   - Se houver conflitos, peça ajuda ao usuário para resolver antes de continuar.
3. Execute `git push origin <branch_atual>`.

## 6. Restauração
1. Se o stash foi executado no passo 3, restaure: `git stash pop`.
2. Informe ao usuário: "Processo concluído e alterações pendentes restauradas."
