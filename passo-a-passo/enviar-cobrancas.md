---
title: Enviar os e-mails de cobrança
parent: Passo a passo
nav_order: 2
---

# Enviar os e-mails de cobrança

## Por que isto importa

Gerar a cobrança dentro do sistema não avisa ninguém sozinho. É o e-mail que chega até o
responsável, com o valor e — quando o grupo cobra online — o link de pagamento. Sem esse
passo, a cobrança existe só para quem olha o painel.

## Passo a passo

1. Confirme que o **envio automático está ligado**, em
   **Configurações → Comunicação → Visão geral**. Desligado, nenhum e-mail sai sozinho —
   útil enquanto você está revisando os modelos, mas precisa estar ligado para cobrar de
   verdade.
2. Se o grupo cobra online, gere o **pedido** de cada cobrança (ou em lote, em
   **Cobranças**, selecionando as cobranças e escolhendo **Gerar pedido agora**). É o
   pedido que cria o link de pagamento — sem ele, o responsável não tem como pagar, mesmo
   que receba o aviso.
3. A partir daí, os e-mails saem sozinhos, nos dias configurados em cada modelo (por
   exemplo, "5 dias antes do vencimento" ou "no dia do vencimento").

   ![E-mail de cobrança recebido pelo responsável, com o valor e o link de pagamento](/assets/img/email-cobranca.png)
4. Se precisar reenviar um lembrete fora do calendário automático — por exemplo, porque um
   responsável perdeu o e-mail — selecione a cobrança em **Cobranças** e use
   **Reenviar lembrete**.

{: .warning }
O Painel avisa quando há cobranças pendentes sem link de pagamento. Se um responsável
reclamar que "não recebeu nada" ou que "não conseguiu pagar", o primeiro lugar para
checar é se a cobrança dele já tem pedido gerado.

## Exemplo

O ciclo de março foi gerado no dia 1º, com vencimento no dia 10. O modelo "Cobrança"
está configurado para sair 5 dias antes do vencimento — ou seja, dia 5. A família Andrade
recebe o e-mail no dia 5, com o valor e o link de pagamento.

{: .warning }
Esse calendário casa com o **dia exato**. Um lembrete configurado para "5 dias antes" é
enviado no dia 5 e só nele: se naquele dia a cobrança ainda não estiver pronta para sair,
aquele lembrete específico não é reenviado depois. Por isso vale gerar os pedidos logo
depois de gerar o ciclo, e não em cima do vencimento.

## O que pode dar errado

- **"Ninguém recebeu o e-mail deste mês"** — confira, nesta ordem: (1) o envio automático
  está ligado em Comunicação; (2) o e-mail do site está mesmo saindo (veja
  [Diagnóstico](/modulos/diagnostico/)); (3) as cobranças têm pedido gerado.
- **Um responsável específico não recebeu** — veja
  [Entregabilidade](/modulos/entregabilidade/): ela mostra, por ciclo, o que foi enviado,
  o que falhou, o que foi ignorado de propósito (para não duplicar envio) e o que ficou
  sem destinatário por falta de e-mail cadastrado.
- **E-mail cadastrado errado** — corrija o cadastro do responsável ou do membro (veja
  [Módulos → Responsáveis](/modulos/responsaveis/)) e use **Reenviar lembrete**.

## Glossário rápido

**Pedido** — o registro no WooCommerce que carrega o link de pagamento. Uma cobrança pode
existir no GE Associados sem ainda ter um pedido; o e-mail de cobrança só sai depois que o
pedido é criado.
