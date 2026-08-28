---
title: Simulador
parent: Módulos
nav_order: 15
---

# Simulador

**Menu:** Cobranças → aba Simulador

Calcula o valor de uma cobrança **sem gerar nada de verdade** — para testar como uma
regra nova vai se comportar antes de rodar um ciclo inteiro com ela, ou para investigar um
valor de cobrança que parece errado.

![Tela do simulador com os três modos — Membro existente, Família e Cenário hipotético — e os campos de ciclo e data prevista de pagamento](/assets/img/simulador-modos.png)

## Modos

- **Membro existente** — simula por uma pessoa já cadastrada.
- **Família** — simula a família inteira de uma vez: todo mundo que ela cobra, num só
  resultado.
- **Cenário hipotético** — você digita idade, tipo, tamanho de família, seção e ramo, sem
  precisar de um cadastro real. Útil para testar "e se" antes de o jovem sequer existir no
  sistema.

{: .tip }
No modo Membro existente e no modo Família, os campos de busca vêm em ordem alfabética e
aceitam **digitar parte do nome para filtrar** — comece a digitar e escolha entre as
sugestões, em vez de rolar a lista inteira. Isso importa em especial aqui: achar o membro
ou a família certa entre centenas costumava ser o gargalo antes de sequer começar a
investigar.

## O que informar

Nos dois modos reais (Membro existente e Família), você escolhe o **ciclo de cobrança** —
que já traz o plano e a data de vencimento juntos, em vez de dois campos separados. Isso
existe de propósito: **evita simular uma combinação de plano e vencimento que não
corresponde a ciclo nenhum**, o que devolveria um resultado com ar de autoridade sobre uma
situação que, na prática, não pode acontecer.

Ainda não gerou o ciclo do período que você quer testar? Marque **"Ainda não há ciclo —
informar plano e vencimento"**: os dois campos reabrem e você preenche à mão, do jeito que
o simulador funcionava antes.

No lugar de "situação de pagamento" e "dias em atraso" — que exigiam fazer a conta de
cabeça antes de simular —, agora você informa só a **data prevista de pagamento** (o
padrão é hoje). O sistema deriva sozinho se está adiantado ou atrasado, e quantos dias.

{: .tip }
Como consequência dessa mudança, o **desconto por pagamento antecipado** agora aparece no
resultado do simulador — antes, a tela não tinha como simular isso, e a regra ficava
invisível até a cobrança de verdade ser gerada.

## O resultado

Mostra o valor base, cada ajuste aplicado com o motivo, e o total. Regras que **não**
entraram aparecem também, com a razão (por exemplo, "idade fora do intervalo") — o que
ajuda a entender por que uma regra que você esperava ver aplicada não apareceu.

Quando existe regra de antecipação ou de multa vigente para aquele ciclo, o resultado
também mostra uma **faixa**: quanto se paga adiantado e quanto se paga em atraso, com as
duas datas-limite nomeadas — por exemplo, "Pagando até 07/12: R$ 95,00 · Pagando a partir
de 13/12: R$ 110,00". Sem nenhuma das duas regras vigentes, a faixa não aparece — não há o
que mostrar.

![Resultado de uma simulação com multa por atraso aplicada e a faixa mostrando quanto se paga até o vencimento e a partir do dia seguinte](/assets/img/simulador-resultado-faixa.png)

### Resultado no modo Família

O modo Família devolve mais informação do que a soma dos membros:

- **Cada membro com o próprio cálculo** — valor, regras aplicadas, e regras consideradas
  e não aplicadas com o motivo, do mesmo jeito que uma simulação individual.
- O **total da família**.
- A lista de **membros da família que não estão sendo cobrados**, com o motivo: fim de
  cobrança, idade fora da faixa do plano, ou limite de cobranças atingido.

![Resultado do modo Família: o cálculo de cada membro, o total da família e a lista de membros não cobrados com o motivo](/assets/img/simulador-resultado-familia.png)

{: .tip }
É o modo certo para investigar desconto de irmãos ou de ramo, porque essas regras
**disputam entre os membros da mesma família** — simular um jovem sozinho não mostra essa
interação. Veja [Antes de cada ciclo](/tesoureiro/inicio-de-ciclo/#o-que-conferir).

## Regras vigentes hoje, não as da cobrança emitida

{: .important }
O simulador sempre calcula com as **regras vigentes no momento em que você simula** —
nunca com as regras que valiam quando uma cobrança específica foi emitida. Para ver o
retrato congelado de uma cobrança já emitida, abra o [detalhe da
cobrança](/modulos/cobrancas/#detalhe-da-cobrança) e olhe a aba **Snapshot de regras**.

Comparar os dois números sem saber dessa diferença é a forma mais comum de concluir, por
engano, que o simulador está errado. Se uma regra mudou entre a emissão da cobrança e
hoje, os dois valores **devem** divergir — e o snapshot é o que explica por quê.

{: .tip }
Este é o simulador de uso **interno**, para quem administra o plugin. Existe também um
[Simulador público](/responsavel/simulador/), acessível a qualquer visitante do site.
