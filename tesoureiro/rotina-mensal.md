---
title: A rotina do mês
parent: Trilha do tesoureiro
nav_order: 2
---

# A rotina do mês

O mesmo roteiro, todo mês, na mesma ordem. A ordem importa: cada passo depende do anterior
ter dado certo.

## 1. Conferir o cadastro

Antes de gerar qualquer coisa, confira quem entrou e quem saiu desde o mês passado — ver
[Entradas e saídas](/tesoureiro/entradas-e-saidas/). Cobrança nasce a partir do cadastro:
o que estiver errado aqui vira erro multiplicado por todo mundo.

## 2. Gerar o ciclo

Em [Ciclos de cobrança](/modulos/ciclos/), escolha o plano, dê um nome ao período (por
exemplo, "Março/2026") e a data de vencimento. **A pré-visualização mostra quantos serão
cobrados antes de você confirmar** — confira esse número contra o que você espera. Se
vierem 40 quando o grupo tem 45 jovens, alguma coisa está errada no cadastro, e é agora
que dá para descobrir.

O passo a passo detalhado está em
[Configurar um plano de cobrança](/passo-a-passo/configurar-plano/).

## 3. Garantir o link de pagamento

Se o grupo cobra online, cada cobrança precisa virar um **pedido** — é o pedido que carrega
o link de pagamento. Em [Cobranças](/modulos/cobrancas/), selecione as cobranças do ciclo e
use **Gerar pedido agora**.

{: .warning }
Cobrança sem pedido **não** recebe lembrete: o sistema segura o e-mail de propósito, porque
não faria sentido pedir que alguém pague sem oferecer como. Você recebe um aviso por e-mail
quando isso acontece, e a [Entregabilidade](/modulos/entregabilidade/) marca essas
cobranças como "pedido não gerado". Não deixe passar: a família não foi avisada.

{: .note }
Enquanto o pedido não existe, o [portal do responsável](/responsavel/portal/) mostra, no
lugar do link de pagamento, a orientação **"Procure a diretoria do grupo para resolver
esta cobrança"** — é assim que a família sabe que precisa falar com vocês em vez de achar
que o sistema travou. O termo "diretoria do grupo" é um rótulo: se o seu grupo usa outro
nome (por exemplo, "coordenação" ou "tesouraria"), troque em
[Rótulos](/modulos/rotulos/).

### Três jeitos de fazer o link chegar até o responsável

Pedido gerado não é o mesmo que responsável avisado. Escolha o caminho pelo canal que a
família usa:

- **Copiar link de pagamento** — no [detalhe da cobrança](/modulos/cobrancas/), copia o
  link direto para a área de transferência. É o mais rápido quando o pedido chega por
  WhatsApp ou é feito na hora, pessoalmente na reunião.
- **Reenviar lembrete** — ação em lote em [Cobranças](/modulos/cobrancas/): dispara de
  novo o e-mail de cobrança, com o botão de pagamento. Serve quando o responsável perdeu o
  e-mail original ou pediu para reenviar.
- **Portal do responsável** — a família pede o próprio acesso, sem depender de vocês. Bom
  padrão para quem prefere resolver sozinho, mas exige que o responsável saiba que o
  [portal](/responsavel/portal/) existe.

## 4. Conferir que os avisos saíram

Um ou dois dias depois, abra [Entregabilidade](/modulos/entregabilidade/) e olhe as cinco
colunas. "Enviado" é o que se espera. "Sem destinatário" quer dizer cadastro incompleto —
alguém sem e-mail. "Falhou" é problema de envio do site, e o
[Diagnóstico](/modulos/diagnostico/) ajuda a achar.

## 5. Dar baixa no que entrou por fora

Pix na conta do grupo, dinheiro entregue na reunião, transferência: nada disso o sistema
enxerga sozinho. Em [Cobranças](/modulos/cobrancas/), use **Confirmar pagamento** com a
data real do pagamento — não a data em que você está registrando.

{: .important }
**Anexe o comprovante.** O campo existe para isso, e é o que permite a qualquer pessoa da
diretoria, no ano que vem, entender por que aquela cobrança está paga sem ter passado pelo
gateway. Se não tiver o comprovante em mãos, marque a opção que diz isso — a escolha fica
registrada no histórico, e é melhor um registro honesto do que um silêncio.

{: .note }
Assim que a cobrança fica paga, o responsável passa a ver o link **Baixar recibo** dela no
[portal](/responsavel/portal/) — e, no fim do ano, a **declaração anual** com tudo que
pagou. São documentos informais, sem valor fiscal; não substituem nota fiscal.

{: .important }
**Marcar o pedido como Concluído ou Processando direto no WooCommerce agora dá baixa
sozinho na cobrança correspondente** — não é mais preciso vir até aqui confirmar de novo.
Isso vale a partir da atualização de agosto/2026 e **não vale para trás**: pedido que já
tinha sido concluído manualmente no WooCommerce **antes** dessa atualização continua com a
cobrança Pendente, porque o sistema não reprocessa mudanças antigas. Encontrou um pedido
assim — pago no WooCommerce, mas a cobrança ainda Pendente aqui? Dê baixa manual, com
**Confirmar pagamento**, do jeito de sempre.

{: .note }
Cobrança que fechou em **R$ 0,00** — por isenção, desconto ou ajuste — nunca aparece nos
passos 3 a 6: ela vira **[Sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)**,
não pede link de pagamento, não entra em lembrete nem em atraso. A família recebe um
e-mail avisando o motivo, uma única vez, e você não precisa fazer nada com ela — só volta
a aparecer aqui se deixar de ser zerada num ciclo futuro.

## 6. Olhar o atraso enquanto ele é pequeno

Em [Inadimplência](/modulos/inadimplencia/), veja quem está devendo e há quanto tempo. As
faixas de atraso existem para priorizar: quem está há 10 dias resolve com um lembrete; quem
está há 90 costuma exigir conversa.

Reenviar o aviso de uma cobrança específica é uma ação de lote em
[Cobranças](/modulos/cobrancas/) — **Reenviar lembrete**.

## 7. Fechar o mês

[Recebimentos](/modulos/recebimentos/) mostra tudo que entrou (e o que foi estornado) no
período, com o valor cobrado ao lado do valor recebido. É o número que vai para a
diretoria, e dá para exportar em CSV.

{: .tip }
A tabela de totais por ramo, em [Composição](/modulos/composicao/), foi feita pensando em
ata de reunião: ela isola quantos associados cada ramo tem, com entradas e saídas do
período.
