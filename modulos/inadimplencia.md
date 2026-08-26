---
title: Inadimplência
parent: Módulos
nav_order: 2
---

# Inadimplência

**Menu:** Painel e Relatórios → aba Inadimplência

Lista de cobranças em atraso, para a tesouraria priorizar quem cobrar primeiro.

![Relatório de inadimplência com valor estimado e faixa de atraso](/assets/img/relatorio-inadimplencia.png)

## O que você vê

Cada linha traz o **valor estimado no dia da geração do relatório** — não é fixo, porque a
multa por atraso muda a cada dia —, os **dias de atraso**, a **faixa de atraso**, o
**vencimento**, o **plano**, o **ciclo** e o **pedido** (o número do pedido WooCommerce).

{: .note }
Esta tela não tem filtro de período. Se você quer recortar a inadimplência por uma data
específica, use [Recebimentos](/modulos/recebimentos/).

{: .note }
Cobrança **[Sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)** nunca
aparece aqui — ela não está em atraso, está zerada.

## Cobrança de família: uma linha, com detalhe por membro

![Relatório de inadimplência com a linha de uma família expandida, mostrando o valor cobrado e pago de cada membro](/assets/img/relatorio-inadimplencia-agrupado.png)

Quando o atraso é de uma **cobrança familiar**, a linha traz uma seta ao lado do nome do
responsável. Clique para ver quem compõe aquele valor: cada membro, com o quanto foi
cobrado dele. Cobrança de **um membro só** continua linha simples, sem seta.

{: .tip }
Útil na hora de ligar para a família: em vez de "vocês devem R$ 90,00", você já sabe que
são dois jovens, R$ 45,00 cada — e qual dos dois entrou na família depois, se um dos
valores destoar do outro.

## O que você faz aqui

- **Seleção múltipla** e **exportação em CSV**, do total ou só da seleção — útil para levar
  a lista para uma reunião de diretoria ou para ligar para os atrasados em ordem.

{: .warning }
Quando a lista é maior do que a tela consegue mostrar de uma vez, o relatório avisa que
truncou o resultado — nesse caso, exporte em CSV para ver a lista completa.

{: .note }
A planilha exportada traz **Plano**, **Período do ciclo** e **Pedido** no fim de cada
linha, depois das colunas que já existiam — a ordem antiga não muda.
