---
title: Antes de instalar
nav_order: 2
---

# Antes de instalar

O GE Associados é um plugin normal de WordPress: instala-se em **Plugins → Adicionar
novo**, como qualquer outro. Antes de ativar, três coisas valem a pena estar prontas —
nenhuma é bloqueante, mas resolver antes economiza retrabalho depois.

## Requisitos técnicos

- **WordPress 6.4** ou mais novo.
- **PHP 8.1** ou mais novo.
- Se o grupo quiser cobrar online (cartão, Pix, boleto pelo site): **WooCommerce 8.0** ou
  mais novo, ativo.

{: .note }
Sem o WooCommerce ativo, o plugin funciona normalmente para cadastro, planos e regras —
só a emissão do link de pagamento fica indisponível. Uma tela do painel avisa quando o
WooCommerce não está ativo.

## Uma organização por instalação

O plugin foi feito para atender **um grupo escoteiro por instalação do WordPress**. Não é
possível cadastrar uma segunda organização no mesmo site — se o seu grupo administra mais
de uma unidade e quer separá-las por completo, cada uma precisa da sua própria instalação
de WordPress com o plugin.

## Meio de pagamento (se for cobrar online)

O GE Associados não processa pagamento — ele cria o pedido e delega ao WooCommerce, que
usa o meio de pagamento que o grupo já tiver configurado (gateway de cartão, Pix, boleto).
Se o grupo pretende cobrar online, configure o WooCommerce e o gateway de pagamento
**antes** de gerar a primeira cobrança — assim o link que sai no e-mail já funciona de
primeira.

{: .tip }
Não tem certeza se o WooCommerce está com um meio de pagamento funcionando? Faça um
pedido de teste de valor baixo antes de gerar a primeira cobrança de verdade.

## Envio de e-mail

O plugin manda e-mails automáticos — cobrança, lembrete, link de acesso ao portal do
responsável, resumo periódico. Esses e-mails saem pelo mecanismo de e-mail do próprio
WordPress. Em muitas hospedagens, o e-mail padrão do WordPress cai em spam ou não chega —
por isso vale confirmar, antes de colocar o plugin em uso, que o site consegue mandar
e-mail de verdade (um plugin de SMTP costuma resolver).

Depois de instalar, use a tela [Diagnóstico](/modulos/diagnostico/) para mandar um e-mail
de teste e confirmar que está chegando.

{: .warning }
Se o e-mail de cobrança não chegar, o responsável não sabe que precisa pagar — e a
tesouraria só descobre quando o prazo já passou. Confirme o envio de e-mail antes de
depender do plugin para cobrar de verdade.
