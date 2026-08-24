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

![Detalhe de uma cobrança, aba Resumo, com regras aplicadas](/assets/img/cobranca-detalhe.png)

Abas: **Resumo** (valor base e os ajustes aplicados), **Snapshot de regras** (o retrato
congelado das regras no momento em que a cobrança foi emitida), **Membros** (numa
cobrança de família, quem entrou e quanto) ou **Detalhes** (numa cobrança individual),
**Notificações** e **Histórico**.

![Detalhe da cobrança, aba Histórico](/assets/img/cobranca-detalhe-historico.png)

Ações disponíveis: confirmar pagamento (data obrigatória, observação, comprovante em
PDF/JPG/PNG até 5 MB — ou marcar que vai anexar depois, o que fica registrado no
histórico), alterar valor com motivo, cancelar com motivo, e tentar gerar o pedido de novo
quando a tentativa anterior falhou.

{: .important }
Editar uma regra **não muda o valor de uma cobrança já emitida** — só afeta cobranças
futuras. A própria tela do detalhe diz isso, para evitar confusão sobre por que o valor
não mudou depois de uma correção na regra.
