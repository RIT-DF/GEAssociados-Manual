---
title: Regras
parent: Módulos
nav_order: 14
---

# Regras

**Menu:** Cobranças → aba Regras

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

## Carência da multa por atraso

Numa regra de **multa**, o campo **carência (dias)** define quantos dias depois do
vencimento a multa ainda **não** incide. Configurando, por exemplo, 5 dias de carência, uma
cobrança paga no 3º dia de atraso não leva multa — só passa a levar a partir do 6º dia.

{: .tip }
É a diferença entre punir todo mundo que atrasa um dia por imprevisto e reservar a multa
para quem realmente demora a pagar. Sem carência configurada (0 dias), a multa incide a
partir do primeiro dia de atraso, como sempre funcionou.

## Alterações não salvas

<!-- CAPTURA PENDENTE: regras-alteracao-nao-salva (desktop) — o aviso de
     saída com alteração pendente, ao tentar fechar a tela de edição de uma
     regra sem salvar. Não capturado nesta sessão: agente em background, sem
     sessão autenticada — o login é do usuário. -->

Se você editar uma regra e tentar sair sem salvar, a tela avisa antes de descartar o que
você mudou. Os botões da tela também dizem, no próprio rótulo, **o que cada um salva** —
por exemplo, se a alteração vira uma nova versão ou atualiza a versão atual — para não
depender de adivinhar pelo nome genérico "Salvar".
