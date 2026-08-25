---
title: Acompanhar um plano de cobrança
parent: Passo a passo
nav_order: 3
---

# Acompanhar um plano de cobrança

## Por que isto importa

Gerar a cobrança é só o começo. O trabalho do mês a mês é saber quem pagou, quem está
atrasado e o que precisa de atenção — sem isso, o grupo descobre a inadimplência tarde
demais, quando já afeta o caixa.

## Passo a passo

### 1. Gerar o ciclo

1. Abra **Cobranças → Ciclos de cobrança**.
2. Escolha o plano.
3. Clique em **Novo ciclo**, informe o período de referência (por exemplo, "mar/2026") e
   a data de vencimento.
4. O sistema mostra uma **prévia de quantos serão cobrados** antes de você confirmar —
   confira o número antes de seguir.
5. Confirme para gerar as cobranças do ciclo.

### 2. Acompanhar pelo Painel

Abra o [Painel](/modulos/painel/) e filtre pelo plano ou ciclo que você acabou de gerar.
Ele mostra quanto já entrou, quanto ainda é esperado, a inadimplência em valor e em
percentual, e uma lista das cobranças mais críticas.

### 3. Confirmar pagamentos

Quando o grupo cobra online pelo WooCommerce, a confirmação costuma ser automática. Para
pagamento fora do sistema (dinheiro, transferência, Pix direto):

1. Abra a cobrança em **Cobranças**, ou selecione várias e use a ação em lote
   **Confirmar pagamento**.
2. Informe a **data do pagamento** e, se quiser, anexe um **comprovante** (PDF, JPG ou PNG,
   até 5 MB) — ou marque que vai anexar depois.

### 4. Tratar exceções

- **Cobrança com valor errado** — abra o detalhe da cobrança e use **Alterar valor**,
  informando o motivo (obrigatório).
- **Cobrança que não deve mais existir** — use **Cancelar**, também com motivo
  obrigatório.

## Exemplo

A tesouraria gerou o ciclo de abril no dia 1º, com 42 cobranças. No Painel, filtrado pelo
ciclo de abril, aparecem 30 pagas, 8 em aberto (ainda dentro do prazo) e 4 vencidas. A
tesoureira abre o relatório de [Inadimplência](/modulos/inadimplencia/), separa as 4
vencidas por tempo de atraso e liga para os dois responsáveis com mais de 15 dias de
atraso — os outros dois ainda estão dentro da tolerância que o grupo costuma dar.

## O que pode dar errado

- **"Gerar pedido" falhou para algumas cobranças** — o acompanhamento do lote mostra cada
  uma como na fila, processando, concluída, recusada ou falha; uma falha parcial aparece
  explicitamente, não vira um "pronto" genérico. Corrija a causa (por exemplo, um cadastro
  incompleto) e tente novamente pela cobrança individual.
- **Editei uma regra e o valor de uma cobrança já emitida não mudou** — é o comportamento
  esperado. Editar uma regra só afeta cobranças futuras; a tela de detalhe da cobrança
  mostra isso explicitamente.
- **Preciso excluir cobranças em lote** — a exclusão em lote mostra, antes de confirmar,
  um ensaio a seco com o que o gateway de pagamento reembolsa automaticamente e o que foi
  pago manualmente e precisará de reembolso à parte, feito por fora do sistema.

## Limites do papel

Confirmar pagamento, cancelar e alterar valor dependem da permissão do seu usuário em
**Configurações → Permissões**. Se algum desses botões não aparecer para você, peça à
coordenação para revisar as permissões do seu papel.
