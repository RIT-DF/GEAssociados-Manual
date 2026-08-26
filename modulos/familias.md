---
title: Famílias
parent: Módulos
nav_order: 7
---

# Famílias

**Menu:** Famílias e Membros → aba Famílias

Uma família é o grupo de cobrança — reúne um ou dois responsáveis financeiros e os
membros ligados a eles.

![Lista de famílias, com uma família expandida mostrando os membros](/assets/img/familias-lista.png)

## O que você faz aqui

Criar, editar, excluir (individualmente ou em lote), expandir uma família para ver seus
membros, e ordenar a lista.

{: .note }
Excluir uma família **não apaga os membros dela** — eles ficam sem família vinculada. A
tela avisa, na confirmação, quantos membros ficarão sem família.

## Campos do cadastro

![Formulário de nova família, com os quatro modos de responsável financeiro](/assets/img/familia-formulario.png)

| Campo | Obrigatório | O que faz |
|---|---|---|
| Primeiro responsável | Sim | |
| Segundo responsável | Não | |
| Responsável financeiro | Sim | Define quem recebe a cobrança — veja abaixo |
| Nome da família | Não | Em branco, o sistema mostra o nome derivado do responsável |

{: .tip }
Os campos **Primeiro responsável** e **Segundo responsável** vêm em ordem alfabética e
aceitam **digitar parte do nome para filtrar** — útil quando o cadastro de responsáveis é
grande. Texto que não bate com nenhum nome exato não é aceito: o campo mantém a seleção
anterior e avisa que não encontrou nada.

### Responsável financeiro — os quatro modos

- **Apenas o primeiro** ou **apenas o segundo** — só essa pessoa recebe a cobrança.
- **Ambos** — cobrança única, que qualquer um dos dois pode quitar.
- **Nenhum** — bolsa integral: a família não gera cobrança nenhuma.

{: .important }
O campo "Responsável financeiro" decide quem recebe o e-mail de cobrança. Configurar
errado manda a cobrança para a pessoa errada, e ninguém percebe até o vencimento passar
sem pagamento.

## Declaração anual

![Modal de declaração anual de uma família, com o campo de ano](/assets/img/familia-declaracao-anual.png)

Cada linha da lista tem o botão **Declaração**, que abre um modal para escolher o **ano**
e baixar um PDF único com tudo que a família pagou naquele ano — o mesmo documento que o
responsável já pode baixar sozinho no [portal](/responsavel/portal/), mas emitido por
você. Útil para quem pede o comprovante direto na secretaria, sem acessar o portal.

Os anos disponíveis são sempre os três mais recentes: o corrente e os dois anteriores.

{: .warning }
A declaração é um documento informal, sem valor fiscal — veja o mesmo aviso em
[Baixar recibo](/modulos/cobrancas/#baixar-recibo-tesouraria).

## Um responsável em mais de uma família

Um mesmo responsável financeiro pode participar de **mais de uma família** — o caso mais
comum é família recomposta, em que um dos responsáveis também é responsável financeiro
noutro núcleo familiar, com outros filhos. Não é preciso duplicar o cadastro da pessoa
para isso: vincule o mesmo responsável às duas famílias.

## Avisos

O sistema avisa quando há um **responsável sem família vinculada** — vale conferir esses
casos, porque um responsável assim não tem como receber cobrança nenhuma.
