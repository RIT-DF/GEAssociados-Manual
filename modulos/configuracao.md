---
title: Importar / Exportar
parent: Módulos
nav_order: 21
---

# Importar / Exportar

**Menu:** Configurações → aba Importar / Exportar

Exportar, importar e apagar a configuração do plugin — não os dados de associados.

![Tela de exportar, importar e excluir configuração](/assets/img/configuracao.png)

## Exportar

Exporta rótulos, ramos, seções, planos, regras e modelos de e-mail. **Nunca** exporta
associados, responsáveis, famílias ou cobranças — é configuração, não dado pessoal.

## Importar

Traz uma configuração exportada de outra instalação, com **ensaio a seco** antes de
aplicar. Para cada item, escolha entre **ignorar**, **atualizar** ou **substituir**;
substituir um item que já tem cobrança ou ciclo vinculado pede confirmação item a item.

{: .note }
A identidade do grupo (nome, sigla, CNPJ, endereço, e-mail financeiro) **não muda** na
importação — só a configuração operacional (planos, regras, rótulos etc.) é afetada.

## Excluir configuração

![Confirmação de exclusão de configuração](/assets/img/configuracao.png)

Mostra o que será removido, exige **digitar o nome exato da organização** para confirmar,
e é **irreversível**.

{: .important }
Excluir a configuração **não toca em associados nem em cobranças** — apenas nos itens de
configuração (planos, regras, rótulos, modelos). Ainda assim, por ser irreversível, use
com cuidado e considere exportar antes.
