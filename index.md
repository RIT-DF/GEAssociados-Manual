---
title: Início
nav_order: 1
---

# Manual do GE-Associados

O **GE-Associados** é o plugin WordPress que a sua organização usa para cadastrar associados,
organizar famílias e responsáveis financeiros, definir regras de cobrança e cobrar
periodicamente — com ou sem pagamento online via WooCommerce.

Este manual segue a ordem em que você normalmente usa o plugin: primeiro configura, depois
cadastra, depois cobra. Se você já sabe o que procura, use a busca no topo da página.

## Por onde começar

**Instalando agora?** Siga [Wizard de onboarding](wizard) — ele guia a configuração inicial em
9 passos e já deixa um plano de cobrança funcionando ao final.

**Já configurado, procurando uma tarefa específica?** Os caminhos mais comuns:

| Eu preciso... | Onde ir |
|---|---|
| Cadastrar associados um a um | [Membros](members), [Famílias](families), [Responsáveis financeiros](responsibles) |
| Trazer uma planilha com os associados atuais | [Importação de planilhas](imports) |
| Definir quanto e quando cobrar | [Planos de cobrança](billing-plans), [Motor de regras](rules-engine) |
| Gerar a cobrança do mês/semestre | [Ciclos de cobrança](billing-cycles) |
| Ver quem pagou, quem deve, cancelar ou corrigir uma cobrança | [Painel de cobranças](charges) |
| Receber pagamento online (PIX, cartão, boleto) | [Integração WooCommerce](woocommerce), [Link de pagamento](pay-link) |
| Configurar os e-mails que o sistema envia | [Configurações de notificação](notification-settings), [Templates de e-mail](notification-templates) |
| Descobrir por que um e-mail não chegou | [Histórico de envios](notification-log) |
| Ter uma visão geral do mês (recebido, inadimplência) | [Dashboard executivo](dashboard) |

## Estrutura do manual

O menu lateral segue os mesmos 10 grupos que você vê dentro do plugin, na mesma ordem:
Visão geral, Começando, Cadastros, Importação, Configuração financeira, Cobrança,
Pagamentos online, Comunicação, Acompanhamento e Próximos passos.

{: .note }
> Este manual descreve o **GE-Associados v1.1.4**. Feito para quem administra a organização —
> coordenação, tesouraria e quem opera o dia a dia dos cadastros e cobranças no wp-admin. Não é
> preciso conhecimento técnico de WordPress ou WooCommerce para acompanhar: onde o assunto exige
> mais, o próprio texto avisa.

## Quem administra o quê

O GE-Associados não distingue papéis de usuário dentro do plugin — quem tem acesso ao menu
**GE-Associados** no wp-admin vê e faz tudo. A separação de responsabilidade é organizacional,
não do sistema:

- **Quem cadastra** — mantém membros, famílias e responsáveis em dia. Ver [Cadastros](branches).
- **Quem configura o financeiro** — define planos e regras de cobrança. Ver
  [Configuração financeira](billing-plans).
- **Quem opera a cobrança** — gera ciclos, confirma pagamentos, acompanha inadimplência. Ver
  [Cobrança](billing-cycles) e [Acompanhamento](dashboard).

Se a sua organização usa capacidades do WordPress para restringir quem acessa o menu
**GE-Associados**, isso é configuração de perfil de usuário do próprio WordPress — o manual não
cobre esse passo porque ele é igual ao de qualquer outro plugin.
