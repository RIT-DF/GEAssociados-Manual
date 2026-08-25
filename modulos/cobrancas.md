---
title: Cobranças
parent: Módulos
nav_order: 11
---

# Cobranças

**Menu:** Cobranças → aba Cobranças

A lista de todas as cobranças, com filtros e ações em lote. É a tela do dia a dia de
quem acompanha pagamentos.

![Lista de cobranças, sem seleção](/assets/img/cobrancas-lista.png)

## Filtros

Status (pendente, aguardando pedido, vencido, paga, cancelada), plano, ciclo, período de
vencimento, e busca por nome ou matrícula.

## Ações em lote

![Lista de cobranças com itens selecionados e a barra de ações em lote](/assets/img/cobrancas-lote.png)

Selecione uma ou várias cobranças (há "selecionar todos") e escolha:

- **Gerar pedido agora** — assíncrono, com acompanhamento item a item (fila, processando,
  concluída, recusada ou falha — sem esconder falha parcial atrás de um "pronto" genérico).
- **Confirmar pagamento**, com data e comprovante.
- **Cancelar**, com motivo obrigatório.
- **Alterar valor**, com motivo obrigatório.
- **Reenviar lembrete**.
- **Exportar em XLSX**.
- **Excluir** — com ensaio a seco antes de confirmar, mostrando o que o gateway de
  pagamento reembolsa automaticamente e o que foi pago manualmente e precisa de reembolso
  à parte.

## Detalhe da cobrança

![Detalhe de uma cobrança, aba Resumo, com identificação, valores e as ações disponíveis](/assets/img/cobranca-detalhe.png)

Abas: **Resumo** (quem é, quanto, quando vence, e as ações), **Snapshot de regras** (o
retrato congelado das regras no momento em que a cobrança foi emitida), **Membros** (numa
cobrança de família, quem entrou e quanto) ou **Detalhes** (numa cobrança individual),
**Notificações** e **Histórico**.

No Resumo, compare **Valor (estimado hoje)** com **Valor de referência (plano, sem
regras)**: se os dois diferem, alguma regra mexeu no valor, e a aba seguinte diz quais.

![Aba Snapshot de regras, listando as regras vigentes quando a cobrança foi emitida](/assets/img/cobranca-detalhe-regras.png)

{: .important }
O snapshot é um **retrato congelado**. Se você renomear uma regra ou mudar um percentual
depois, esta tela continua mostrando o que valia no dia da emissão — é assim que se
descobre, meses depois, por que aquela cobrança saiu naquele valor. Mudança em regra afeta
só cobrança futura, nunca a que já foi emitida.

![Detalhe da cobrança, aba Histórico](/assets/img/cobranca-detalhe-historico.png)

Ações disponíveis: confirmar pagamento (data obrigatória, observação, comprovante em
PDF/JPG/PNG até 5 MB — ou marcar que vai anexar depois, o que fica registrado no
histórico), alterar valor com motivo, cancelar com motivo, e tentar gerar o pedido de novo
quando a tentativa anterior falhou.

## Copiar link de pagamento

<!-- CAPTURA PENDENTE: cobranca-detalhe-copiar-link (desktop + mobile) —
     detalhe de uma cobrança Pendente com pedido válido, botão visível.
     Não capturado nesta sessão: o Playwright estava em uso por outra sessão
     no momento da execução. -->

Quando a cobrança está **Pendente** e o pedido ainda aceita pagamento, o detalhe mostra o
botão **Copiar link de pagamento**. Um clique copia o endereço para a área de transferência
— é o jeito mais rápido de mandar o link para quem pediu por WhatsApp ou pessoalmente, sem
esperar o próximo e-mail automático.

{: .note }
O botão só aparece quando faz sentido usá-lo. Se o pedido **não aceita mais pagamento** —
porque já foi marcado como concluído ou foi cancelado direto no WooCommerce, fora do
GE Associados — o botão some e a tela explica: *"Este pedido não aceita mais pagamento —
provavelmente já foi concluído ou cancelado diretamente no WooCommerce."* Não é erro do
sistema: é o pedido dizendo que aquele caminho não serve mais. Confira o status da
cobrança (pode já estar paga) antes de procurar o link em outro lugar.

Veja as outras duas formas de fazer o link chegar até o responsável em
[A rotina do mês](/tesoureiro/rotina-mensal/#3-garantir-o-link-de-pagamento).

{: .important }
Editar uma regra **não muda o valor de uma cobrança já emitida** — só afeta cobranças
futuras. A própria tela do detalhe diz isso, para evitar confusão sobre por que o valor
não mudou depois de uma correção na regra.
