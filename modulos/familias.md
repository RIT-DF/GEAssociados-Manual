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

### Responsável financeiro — os quatro modos

- **Apenas o primeiro** ou **apenas o segundo** — só essa pessoa recebe a cobrança.
- **Ambos** — cobrança única, que qualquer um dos dois pode quitar.
- **Nenhum** — bolsa integral: a família não gera cobrança nenhuma.

{: .important }
O campo "Responsável financeiro" decide quem recebe o e-mail de cobrança. Configurar
errado manda a cobrança para a pessoa errada, e ninguém percebe até o vencimento passar
sem pagamento.

## Avisos

O sistema avisa quando há um **responsável sem família vinculada** — vale conferir esses
casos, porque um responsável assim não tem como receber cobrança nenhuma.
