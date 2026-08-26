---
title: Recebimentos
parent: Módulos
nav_order: 3
---

# Recebimentos

**Menu:** Painel e Relatórios → aba Recebimentos

Todo o dinheiro que entrou — ou saiu, em caso de reembolso — no período escolhido.

![Relatório de recebimentos com entradas e reembolsos do período](/assets/img/relatorio-recebimentos.png)

## O que você vê

Cada entrada e cada reembolso do período, com data, tipo, quem pagou, **plano**, **ciclo**,
**pedido** (o número do pedido WooCommerce — o mesmo que aparece no extrato e no Pix), o
valor cobrado, o valor efetivamente recebido e a forma de pagamento. Reembolsos aparecem
destacados em vermelho, para não passar despercebidos numa lista longa.

## Cobrança de família: uma linha, com detalhe por membro

![Tela de Recebimentos: a cobrança da Família Peixoto Andrade expandida, mostrando os três membros com valor cobrado e pago de cada um; abaixo, uma cobrança individual, que não expande](/assets/img/relatorio-recebimentos-agrupado.png)

Quando o recebimento é de uma **cobrança familiar**, a linha traz uma seta ao lado do
nome do responsável. Clique para abrir o detalhe: cada membro que compõe aquele valor,
com quanto foi cobrado e quanto foi pago dele. Cobrança de **um membro só** continua
linha simples, sem seta — não há o que detalhar.

{: .note }
Por que isso importa: numa família com mais de um jovem, "o valor pago pela família" não
diz **quem** pesou quanto no total — e com mais de um ciclo por ano, a coluna Ciclo é o
que diz a que período aquele recebimento pertence, sem você ter que abrir o pedido no
WooCommerce para descobrir.

## O que você faz aqui

- **Filtro De/Até**, obrigatório — o padrão é o mês corrente.
- **Seleção múltipla** e **exportação em CSV**.

{: .tip }
Esta é a tela certa para fechar as contas de um mês específico — diferente da
Inadimplência, que não tem filtro de data porque olha para o que está em aberto agora,
independente de quando venceu.

{: .note }
A planilha exportada traz as três colunas novas — **Plano**, **Período do ciclo** e
**Pedido** — no fim de cada linha, depois das colunas que já existiam; a ordem antiga não
muda. Repare que o CSV chama a coluna de **"Período do ciclo"**, não só "Ciclo" como na
tela — é a mesma informação, só o rótulo muda entre as duas.
