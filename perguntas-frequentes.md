---
title: Perguntas frequentes
nav_order: 11
---

# Perguntas frequentes

Dúvidas que aparecem com frequência sobre o **comportamento** do plugin — por que ele faz
o que faz.

{: .note }
Se algo parou de funcionar ou apareceu mensagem de erro, o lugar é
[Problemas e soluções](/problemas-solucoes/). Se a situação pede uma ordem certa de
passos, veja [Casos especiais](/casos-especiais/).

## O recibo e a declaração anual têm valor fiscal?

Não. Os dois são documentos **informais**, pensados para você organizar e comprovar a
prestação de contas do grupo — não substituem nota fiscal nem recibo com validade
jurídica. Se alguém precisar de um documento com valor fiscal, isso é conversa com a
diretoria do grupo, fora do plugin. Veja
[Baixar recibo](/modulos/cobrancas/#baixar-recibo-tesouraria) e
[Documentos](/responsavel/portal/#documentos).

## O que é aquele código impresso no rodapé do recibo e da declaração?

É um **identificador da emissão** — uma sequência única, gerada de novo cada vez que o
documento é baixado. Ele serve para você identificar qual emissão é qual quando precisar
comparar duas cópias, nada além disso.

{: .warning }
Ele **não é um selo de autenticidade**. Não existe (nem está previsto) um lugar para
conferir esse código contra o sistema. Não prometa isso a quem perguntar — trate como um
número de controle interno, não como prova de que o documento é genuíno.

## Por que um e-mail do plugin saiu de um endereço diferente do que está configurado?

Porque, depois que o plugin monta e entrega o e-mail, o **próprio WordPress** — ou algum
outro plugin instalado no site, ou o servidor de envio — pode reescrever o remetente por
conta própria. Isso acontece fora do alcance do GE Associados: ele não tem como impedir
essa reescrita, só percebê-la.

Quando isso acontece, o plugin **detecta a divergência** entre o remetente pedido e o
remetente efetivo, e avisa em [Diagnóstico](/modulos/diagnostico/) e em
[Comunicação](/modulos/comunicacao/). Corrigido o remetente na origem, o aviso some
sozinho — não é preciso limpar nada manualmente.

## Por que o link do recibo, no e-mail, me leva para o portal em vez de abrir o PDF direto?

Porque o recibo contém dado de pagamento de uma pessoa específica, e o portal existe
justamente para confirmar **quem está pedindo** antes de entregar esse documento. Não é
um erro do link: é o portal pedindo para confirmar identidade antes de mostrar qualquer
recibo. Veja [O que você vê ao entrar](/responsavel/portal/#o-que-você-vê-ao-entrar).

## Por que o valor de uma cobrança muda conforme a data em que a pessoa paga?

Porque desconto por antecipação e multa por atraso são calculados **na data do
pagamento**, não na data em que a cobrança foi gerada — o valor de uma cobrança pendente é
sempre uma estimativa para "se pagar hoje". É por isso que o detalhe da cobrança mostra um
**Valor (estimado hoje)** ao lado do **Valor de referência**: o primeiro muda dia a dia
até o pagamento acontecer; o segundo, não. Veja
[Detalhe da cobrança](/modulos/cobrancas/#detalhe-da-cobrança) e
[Carência da multa por atraso](/modulos/regras/#carência-da-multa-por-atraso).

## Uma cobrança "Sem valor a pagar" gera recibo?

Não. O recibo comprova um pagamento, e uma cobrança **Sem valor a pagar** nunca chega a
ser paga — não há o que comprovar. Em vez de recibo, essa cobrança dispara um e-mail
próprio, uma única vez, avisando que não há valor devido naquele ciclo. Veja
[Cobrança sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar).

## Os modelos de e-mail que eu personalizei recebem as melhorias que o plugin lança depois?

Só se você adicionar o marcador manualmente. Uma atualização do plugin pode acrescentar
algo a um modelo padrão — por exemplo, a lista de membros que compõem uma cobrança de
família —, e isso aparece sozinho em quem **não mexeu** naquele modelo. Mas modelo que
você já personalizou fica **exatamente como você deixou**: a atualização nunca sobrescreve
texto que você editou. Para incluir uma novidade dessas no seu modelo, adicione o marcador
correspondente você mesmo — veja
[Editar modelo](/modulos/comunicacao/#editar-modelo).

## O que acontece quando eu desativo um membro?

Ele para de contar para tudo: sai da geração de cobrança dali para a frente, sai da
contagem de composição do grupo, e some das listas de membros ativos. As cobranças
**passadas** dele continuam existindo, pagas ou não — desativar não apaga histórico, só
interrompe o que viria depois.

{: .note }
Isso é diferente de só parar de cobrar alguém que continua ativo no grupo — para esse
caso, existe a **Data de fim de cobrança**, um campo separado. Veja a distinção completa,
com a ordem que evita cobrar quem já saiu, em
[Casos especiais](/casos-especiais/#5-um-jovem-se-afastou-do-grupo).
