---
title: Regras
parent: Módulos
nav_order: 14
---

# Regras

**Menu:** Cobranças → Regras

Descontos, acréscimos, multas e isenções que ajustam o valor de uma cobrança. Cada regra
é um filtro (quem ela alcança) mais uma transformação (o que ela faz com o valor).

![Lista de regras cadastradas](/assets/img/regras-lista.png)

## Tipos de regra

Desconto, acréscimo, multa, desconto por antecipação, crédito ou cancelamento.

## Versionamento

![Uma regra aberta, mostrando as versões](/assets/img/regra-versoes.png)

As regras são versionadas: cada versão tem número, vigência (com fim aberto), prioridade
(a de menor número entra primeiro), se acumula com outras regras, os parâmetros e as
condições — idade, tipo de membro, seção, ramo, plano, situação de pagamento e tamanho da
família.

{: .important }
O cálculo de uma cobrança usa a **versão vigente na data em que ela foi gerada**. Editar
uma versão afeta só as cobranças que ainda não foram geradas; para preservar a versão
antiga intacta, salve como uma **nova versão** em vez de editar a existente. Há também a
opção **"fechar hoje"**, que encerra a vigência de uma versão sem apagar seu histórico.

## Reordenar prioridades

O modo de reordenar reescreve as prioridades das regras como 10, 20, 30 — deixando espaço
para inserir uma nova regra entre duas existentes sem precisar renumerar tudo.
