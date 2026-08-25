---
title: Entregabilidade
parent: Módulos
nav_order: 5
---

# Entregabilidade

**Menu:** Painel e Relatórios → aba Entregabilidade

Mostra, por ciclo de cobrança, se os e-mails realmente chegaram aos responsáveis.

![Relatório de entregabilidade por ciclo, com as cinco situações de envio somadas no topo e detalhadas por ciclo na tabela](/assets/img/relatorio-entregabilidade.png)

## O que você vê

Por ciclo, cada e-mail cai em uma de cinco situações:

| Situação | O que significa | O que fazer |
|---|---|---|
| **Enviado** | Saiu e o servidor aceitou | Nada |
| **Falhou** | O servidor de e-mail recusou | Ver [Diagnóstico](/modulos/diagnostico/) — costuma ser configuração de envio do site |
| **Ignorado** | Descartado de propósito, porque a mesma mensagem já tinha saído hoje | Nada — é proteção contra e-mail repetido, não é erro |
| **Sem destinatário** | Não havia e-mail cadastrado para aquela cobrança | Cadastrar o e-mail do responsável ou do associado |
| **Pedido não gerado** | A cobrança ainda não virou pedido, então não existe link de pagamento | Gerar o pedido em [Cobranças](/modulos/cobrancas/) |

{: .tip }
Se um responsável reclamar que não recebeu a cobrança, esta é a tela para verificar antes
de qualquer outra coisa. As cinco situações têm causas diferentes e soluções diferentes —
"falhou" é problema de envio do site, "sem destinatário" é cadastro incompleto, e
"pedido não gerado" é cobrança que ainda não está pronta para ser paga.

{: .important }
**"Pedido não gerado" é o único que representa aviso que o responsável não recebeu por
decisão do sistema.** Enquanto a cobrança não tiver link de pagamento, o lembrete é
segurado de propósito — não faria sentido pedir que alguém pague sem oferecer como. O
financeiro recebe um aviso por e-mail quando isso acontece, e o Painel também sinaliza.

## O que você faz aqui

- **Filtro De/Até**, seleção múltipla e exportação em CSV.
