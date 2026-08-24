---
title: Simulador
parent: Módulos
nav_order: 15
---

# Simulador

**Menu:** Cobranças → Simulador

Calcula o valor de uma cobrança **sem gerar nada de verdade** — para testar como uma
regra nova vai se comportar antes de rodar um ciclo inteiro com ela.

![Simulador com um resultado calculado](/assets/img/simulador.png)

## Modos

- **Real** — simula por um membro ou família já cadastrados.
- **Hipotético** — você digita idade, tipo, tamanho de família, seção e ramo, sem precisar
  de um cadastro real.

Em ambos, informe o plano, a data de vencimento e a situação de pagamento — que muda
quais regras entram no cálculo.

## O resultado

Mostra o valor base, cada ajuste aplicado com o motivo, e o total. Regras que **não**
entraram aparecem também, com a razão (por exemplo, "idade fora do intervalo") — o que
ajuda a entender por que uma regra que você esperava ver aplicada não apareceu.

{: .tip }
Este é o simulador de uso **interno**, para quem administra o plugin. Existe também um
[Simulador público](/responsavel/simulador/), acessível a qualquer visitante do site.
