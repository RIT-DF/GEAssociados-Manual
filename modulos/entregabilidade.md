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

Por ciclo, cada e-mail cai em uma de seis situações:

| Situação | O que significa | O que fazer |
|---|---|---|
| **Enviado** | Saiu e o servidor aceitou | Nada |
| **Falhou** | O servidor de e-mail recusou | Ver [Diagnóstico](/modulos/diagnostico/) — costuma ser configuração de envio do site |
| **Ignorado** | Descartado de propósito, porque a mesma mensagem já tinha saído hoje | Nada — é proteção contra e-mail repetido, não é erro |
| **Sem destinatário** | Não havia e-mail cadastrado para aquela cobrança | Cadastrar o e-mail do responsável ou do associado |
| **Pedido não gerado** | A cobrança ainda não virou pedido, então não existe link de pagamento | Gerar o pedido em [Cobranças](/modulos/cobrancas/) |
| **Link de pagamento indisponível** | O pedido existe, mas não aceita mais pagamento — já foi concluído ou cancelado direto no WooCommerce | Conferir o status da cobrança; se ainda precisa cobrar, gerar um pedido novo |

{: .tip }
Se um responsável reclamar que não recebeu a cobrança, esta é a tela para verificar antes
de qualquer outra coisa. As situações têm causas diferentes e soluções diferentes —
"falhou" é problema de envio do site, "sem destinatário" é cadastro incompleto, "pedido
não gerado" é cobrança que ainda não está pronta para ser paga, e "link de pagamento
indisponível" é um pedido que já saiu de circulação.

{: .important }
**"Pedido não gerado" e "Link de pagamento indisponível" são os únicos que representam
aviso que o responsável não recebeu por decisão do sistema.** Nos dois casos, o lembrete é
segurado de propósito — não faria sentido pedir que alguém pague sem oferecer como, ou
oferecer um link que não funciona mais. O financeiro recebe um aviso por e-mail quando
isso acontece, e o Painel também sinaliza.

### Cada número abre a lista de quem o compõe

<!-- CAPTURA PENDENTE: entregabilidade-detalhe-situacao (desktop) — a lista
     de destinatários por trás de um número da tabela, com o motivo real da
     falha em cada linha. Não capturado nesta sessão: agente em background,
     sem sessão autenticada — o login é do usuário. -->

Clique em qualquer número da tabela para abrir a lista de quem está por trás dele — nome,
cobrança e o **motivo real** daquela falha específica, em vez de precisar cruzar a tabela
resumida com a lista de cobranças por fora.

## O que você faz aqui

- **Filtro De/Até**, seleção múltipla e exportação em CSV.

{: .note }
A exportação traz **uma linha por tentativa de envio**, não só o resumo por ciclo — se um
e-mail foi tentado, falhou e foi reenviado depois, aparecem as duas tentativas
separadamente, cada uma com sua data e seu status.
