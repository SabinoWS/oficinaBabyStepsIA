---
name: Historia de Usuario Writer Expert
description: Use quando precisar escrever, revisar ou refinar historias de usuario com criterio INVEST, criterios de aceite testaveis e cenarios Given-When-Then.
---

# Historia de Usuario Writer Expert

Esta skill guia a escrita de historias de usuario claras, testaveis e orientadas a valor de negocio.

## Objetivo

Produzir uma historia de usuario pronta para desenvolvimento e teste, com:
- Contexto de negocio
- Declaracao da historia (COMO/QUERO/PARA)
- Criterios de aceite objetivos
- Cenarios de teste funcionais
- Escopo e restricoes explicitas

## Fluxo de Trabalho

1. Entender o problema
- Identifique quem e o usuario afetado.
- Identifique dor atual e resultado esperado.
- Confirme o objetivo de negocio em uma frase.

2. Definir escopo minimo
- Delimite o que entra nesta historia (in-scope).
- Delimite o que fica fora (out-of-scope).
- Se o escopo estiver grande, quebre em historias menores.

3. Escrever a historia base
- Use o formato:
  - COMO [perfil]
  - QUERO [capacidade]
  - PARA [beneficio de negocio ou usuario]

4. Construir criterios de aceite
- Escreva criterios verificaveis e sem ambiguidade.
- Evite termos vagos como "rapido", "facil" ou "intuitivo" sem metrica.
- Inclua regras de validacao, permissoes e mensagens de erro quando aplicavel.

5. Escrever cenarios de teste (Gherkin)
- Cubra pelo menos:
  - Fluxo feliz
  - Falha de validacao
  - Permissao/acesso (quando houver regra de perfil)
- Use:
  - DADO QUE [contexto inicial]
  - QUANDO [acao]
  - ENTAO [resultado esperado]

6. Revisar qualidade (checklist)
- A historia atende INVEST?
- Os criterios sao testaveis e independentes?
- Existe dependencia externa bloqueante?
- O valor de negocio ficou explicito?

## Decisoes e Ramificacoes

- Se faltar contexto de negocio:
  - Pausar escrita final e pedir objetivo, publico e impacto.

- Se a historia estiver ampla demais:
  - Dividir por jornada, regra de negocio ou canal (web/mobile/api).

- Se houver dependencia externa forte:
  - Registrar no bloco "Dependencias" e avaliar criar historia tecnica separada.

- Se nao houver criterio de pronto claro:
  - Definir DoD minimo antes de concluir.

## Template Obrigatorio

Use este modelo ao gerar a entrega:

```markdown
[TITULO] Historia de Usuario - [funcionalidade]

Contexto:
- Problema atual:
- Objetivo de negocio:
- Indicador de sucesso (opcional):

Historia:
COMO [tipo de usuario]
QUERO [objetivo funcional]
PARA [beneficio/valor]

Escopo:
- In-scope:
- Out-of-scope:

Criterios de Aceite:
1. [criterio testavel]
2. [criterio testavel]
3. [criterio testavel]

Cenarios (Given-When-Then):
Cenario 1 - Fluxo feliz
DADO QUE [contexto]
QUANDO [acao]
ENTAO [resultado]

Cenario 2 - Validacao
DADO QUE [contexto]
QUANDO [acao invalida]
ENTAO [mensagem/erro esperado]

Cenario 3 - Permissao (se aplicavel)
DADO QUE [perfil sem permissao]
QUANDO [tentativa de acao]
ENTAO [bloqueio esperado]

Dependencias:
- [sistema/time/contrato]

Observacoes:
- [regras complementares]
```

## Criterios de Conclusao

Considere a historia pronta quando:
- O valor de negocio estiver claro para qualquer pessoa do time.
- Os criterios de aceite permitirem teste sem interpretacao subjetiva.
- Os cenarios cobrirem sucesso e principal falha.
- O escopo estiver pequeno o suficiente para caber em uma entrega incremental.
