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

Status (pendente, aguardando pedido, vencido, paga, cancelada, **sem valor a pagar**),
plano, ciclo, período de vencimento, e busca por nome ou matrícula.

## Cobrança sem valor a pagar

Quando o cálculo de uma cobrança fecha em **R$ 0,00** — uma regra zerou o valor, um
desconto encostou no total, ou você mesmo ajustou o valor para zero —, ela deixa de seguir
o fluxo comum e ganha o status **Sem valor a pagar**.

{: .note }
**O gatilho é a cobrança estar zerada, não a pessoa ser isenta.** "Isento" descreve uma
característica de alguém; "sem valor a pagar" é um fato de **uma cobrança, num ciclo
específico**. Um jovem com desconto de irmão pode ter uma cobrança zerada num mês sem ser
isento de nada — a regra de desconto por antecipação, por exemplo, pode zerar o valor só
naquele período. Por isso o status é recalculado a cada cobrança, não herdado do cadastro
da pessoa.

Enquanto estiver nesse status, a cobrança:

- **não** entra na fila de lembretes de vencimento nem de atraso, e nunca chega ao aviso
  formal de inadimplência;
- **não** aparece como pendência no [Painel](/modulos/painel/) nem na
  [Inadimplência](/modulos/inadimplencia/);
- **não** gera pedido novo no WooCommerce — não há o que pagar, então não há link de
  pagamento a oferecer;
- dispara **um** e-mail próprio, uma única vez — veja
  [Comunicação](/modulos/comunicacao/#cobrança-sem-valor-a-pagar).

{: .tip }
Se a cobrança deixar de ser zerada depois — a isenção acabou, a regra mudou, você corrigiu
o valor à mão —, ela **volta sozinha** ao fluxo normal na próxima verificação e passa a
receber a sequência de cobrança dali em diante. Não é preciso reabrir nem recriar nada.

## Nova cobrança avulsa

<!-- CAPTURA PENDENTE: cobranca-avulsa-formulario (desktop) — o formulário de
     nova cobrança avulsa, com os campos de busca de família/membro, ciclo e
     valor calculado. Não capturado nesta sessão: agente em background, sem
     sessão autenticada — o login é do usuário. -->

Além das cobranças que nascem de um ciclo gerado para todo mundo, dá para criar uma
cobrança **avulsa** para uma família ou um membro específico, dentro de um ciclo já
existente — útil para quem entrou no meio do caminho e ficou de fora da geração
automática, ou para cobrar um caso isolado sem esperar o próximo ciclo inteiro.

O valor é **calculado**, do mesmo jeito que uma cobrança normal: passa pelo plano e pelas
regras vigentes, não é digitado à mão.

{: .tip }
Os campos de **família** e de **membro** vêm em ordem alfabética e aceitam **digitar parte
do nome para filtrar** — comece a digitar e escolha entre as sugestões que aparecem, em vez
de rolar a lista inteira. Se o texto digitado não bater com nenhum nome exato, o campo
mantém a seleção anterior e avisa que não encontrou nada — não dá para digitar um nome
parecido e sair do campo esperando que ele escolha sozinho.

{: .important }
O sistema **recusa** criar uma cobrança avulsa quando já existe, para aquela família ou
membro, uma cobrança **não cancelada** no mesmo ciclo — evita duplicar cobrança para
quem já foi cobrado. Cancele a cobrança existente primeiro, se for o caso.

## Ações em lote

![Lista de cobranças com itens selecionados e a barra de ações em lote](/assets/img/cobrancas-lote.png)

Selecione uma ou várias cobranças (há "selecionar todos") e escolha:

- **Gerar pedido agora** — assíncrono, com acompanhamento item a item (fila, processando,
  concluída, recusada ou falha — sem esconder falha parcial atrás de um "pronto" genérico).
  Cobrança **Sem valor a pagar** é recusada aqui — não há valor a cobrar, então não há
  pedido a gerar.
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

![Detalhe de uma cobrança pendente, com o botão "Copiar link de pagamento" ao lado do pedido vinculado](/assets/img/cobranca-detalhe-copiar-link.png)

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

## Baixar recibo (tesouraria)

![Detalhe de uma cobrança paga, com o botão "Baixar recibo" na aba Resumo](/assets/img/cobranca-detalhe-baixar-recibo.png)

Cobrança **paga** ganha, na aba Resumo, o botão **Baixar recibo** — o mesmo PDF que o
responsável já pode baixar sozinho no [portal](/responsavel/portal/), mas emitido por
você. Útil quando alguém pede o comprovante numa reunião presencial, ou quando o
responsável não tem acesso ao portal.

O recibo traz a identidade visual do grupo (logo e cor cadastrados em
[Unidade Escoteira](/modulos/unidade-escoteira/)) e um **identificador da emissão**
impresso no rodapé — uma sequência única, gerada a cada vez que o documento é baixado.

{: .warning }
**O recibo e a declaração anual são documentos informais, sem valor fiscal.** Servem para
comprovar e organizar a prestação de contas do grupo — não substituem nota fiscal. O
identificador impresso no rodapé **não é um selo de autenticidade**: ele identifica aquela
emissão, e não existe (nem está previsto) lugar para conferi-lo.

{: .note }
O botão só aparece com a cobrança **Paga**. Cobrança pendente ou vencida não tem recibo —
não haveria o que comprovar ainda.

{: .important }
Editar uma regra **não muda o valor de uma cobrança já emitida** — só afeta cobranças
futuras. A própria tela do detalhe diz isso, para evitar confusão sobre por que o valor
não mudou depois de uma correção na regra.
