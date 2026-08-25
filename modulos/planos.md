---
title: Planos de cobrança
parent: Módulos
nav_order: 13
---

# Planos de cobrança

**Menu:** Cobranças → aba Planos de cobrança

O que se cobra: valor, periodicidade e como a cobrança é montada. Veja o passo a passo
completo em [Configurar um plano de cobrança](/passo-a-passo/configurar-plano/).

![Lista de planos de cobrança](/assets/img/planos-cobranca.png)

## Campos

![Formulário de novo plano de cobrança](/assets/img/plano-formulario.png)

| Campo | O que faz |
|---|---|
| Nome | |
| Frequência | Mensal, trimestral, semestral, anual ou avulsa |
| Valor base | Valor de tabela, antes de regras |
| Modo de cobrança | Individual, familiar ou híbrido |
| Modo de vencimento | Dia fixo do mês, relativo a um evento, ou definido em cada ciclo |
| Categoria de produto do WooCommerce | Para quem cobra online |

{: .tip }
O **preset escoteiro** cria um plano e três regras prontas de uma vez — e ignora o que já
existir, em vez de duplicar. Bom ponto de partida na primeira configuração.

{: .warning }
**Renomeie o que o preset criar.** O plano e as três regras nascem com o sufixo
`(preset escoteiro)` no nome — marcador de origem, útil para você. Mas o nome da regra é
exibido no [simulador público](/responsavel/simulador/), onde quem ainda não faz parte do grupo
lê a explicação do valor. "Desconto Familiar (preset escoteiro)" numa página voltada a
pais soa como recado interno. Tire o sufixo depois de aplicar o preset.

{: .warning }
**Plano com ciclo já gerado não pode ser excluído.** Resolva as cobranças do ciclo
primeiro (por exemplo, cancelando-as) se precisar remover um plano criado por engano.
