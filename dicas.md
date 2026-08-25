---
title: Dicas
nav_order: 8
---

# Dicas

Um apanhado de práticas que tiram melhor proveito do plugin, para quem já passou dos
primeiros passos.

## Cadastro

- **Cadastre a data de ingresso do membro**, mesmo que pareça óbvio. Ela decide o cálculo
  de pró-rata quando alguém entra no meio de um período de cobrança — deixar em branco faz
  o sistema assumir a data do cadastro, o que nem sempre é a data real de entrada no grupo.
- **Use "Sem CPF (estrangeiro)"** só quando for o caso real. CPF é o principal jeito de o
  sistema reconhecer que duas pessoas cadastradas são a mesma — pular esse campo sem
  necessidade abre espaço para cadastro duplicado.

## Famílias e responsável financeiro

- **Confira o campo "Responsável financeiro"** ao criar cada família. Ele decide quem
  recebe a cobrança — errar aqui manda o e-mail para a pessoa errada, e ninguém percebe até
  o vencimento passar.
- **"Nenhum" é para bolsa integral.** Uma família marcada assim não gera cobrança nenhuma
  — é o jeito certo de tratar um caso de isenção total, sem precisar cancelar cobranças
  manualmente todo mês.

## Regras

- **Cadastre a regra antes de gerar o ciclo**, não depois. Regra criada depois de o ciclo
  já ter sido gerado só vale para o próximo ciclo — a cobrança que já existe não recalcula.
- **Use "fechar hoje"** em vez de apagar uma versão de regra que não serve mais. Isso
  preserva o histórico de cálculo de quem já foi cobrado com aquela versão, em vez de
  apagar o rastro.

## Comunicação

- **Revise os modelos de e-mail com o envio automático desligado.** Assim dá para testar a
  pré-visualização e ajustar o texto sem risco de mandar e-mail errado para os
  responsáveis de verdade.
- **Configure o resumo periódico** para quem cuida da tesouraria — economiza a rotina de
  entrar no painel só para conferir se está tudo em ordem.

## Antes de decisões que não voltam

- **Simule antes de cobrar.** O [Simulador](/modulos/simulador/) calcula o valor de uma
  cobrança sem gerar nada de verdade — use-o para conferir se uma regra nova está
  calculando como esperado antes de rodar um ciclo inteiro com ela.
- **Use o ensaio a seco da exclusão em lote.** Antes de excluir cobranças, o sistema mostra
  o que seria reembolsado automaticamente e o que precisaria de reembolso manual — vale a
  pena ler com calma antes de confirmar.
