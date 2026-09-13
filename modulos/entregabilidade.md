---
title: Entregabilidade
parent: Módulos
nav_order: 5
---

# Entregabilidade

**Menu:** Painel e Relatórios → aba Entregabilidade

Mostra, por ciclo de cobrança, se os e-mails realmente chegaram aos responsáveis — e deixa
corrigir e reenviar direto daqui, sem precisar caçar cada caso por fora.

![Relatório de entregabilidade por ciclo, com as cinco situações de envio somadas no topo e detalhadas por ciclo na tabela](/assets/img/relatorio-entregabilidade.png)

## Filtros

**Plano, ciclo e período** — o mesmo recorte compartilhado das outras abas de Relatórios
(veja [Painel](/modulos/painel/#o-que-você-vê)): filtrar aqui e trocar de aba mantém a
escolha.

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

## Comunicações com problema

![Lista "Comunicações com problema" sempre visível, com o motivo em linguagem simples e a ação sugerida](/assets/img/entregabilidade-lista-problemas-desktop.png)

![A mesma lista "Comunicações com problema" em celular](/assets/img/entregabilidade-lista-problemas-mobile.png)

Abaixo dos cartões e da tabela por ciclo, a lista **Comunicações com problema** fica
**sempre visível** — antes era preciso clicar num número para descobrir que ela existia.
Cada linha traz o nome, a cobrança, o **motivo em linguagem simples** (não o texto cru que
o servidor de e-mail devolveu) e uma **ação sugerida**: corrigir cadastro ou tentar de
novo, conforme o caso.

{: .tip }
Se um responsável reclamar que não recebeu a cobrança, esta lista é o primeiro lugar a
olhar — o motivo já vem traduzido, sem precisar interpretar erro de servidor de e-mail.

### Cartões e tabela filtram a lista

Clique em qualquer **cartão** do topo ou em qualquer **número da tabela por ciclo** para
que a lista abaixo mostre só aquele grupo — por exemplo, só as falhas de um ciclo
específico, ou só os itens "sem destinatário" de todos os ciclos. Um botão **Limpar
filtro** volta a mostrar tudo.

### Corrigir e-mail

Na linha de um item **sem destinatário** ou com e-mail claramente errado, o botão
**Corrigir e-mail** leva direto ao cadastro do responsável ou do membro **já em modo de
edição** — complete o e-mail e volte para a Entregabilidade, no mesmo filtro em que você
estava, sem precisar navegar até a família por fora.

## Reenvio em lote

![Confirmação de reenvio em lote, mostrando quantas comunicações serão reenviadas e quantas ficarão de fora, com o motivo](/assets/img/entregabilidade-lote-confirmacao.png)

Selecione várias linhas (ou use "selecionar todos os que falharam") e reenvie de uma vez.
Antes de sair, a confirmação diz **quantas comunicações serão reenviadas e quantas ficarão
de fora** — por exemplo, itens sem destinatário, que não têm para onde reenviar. Depois de
processar, o resultado aparece **item por item**: enviados, recusados por alguma regra (como
a de não repetir no mesmo dia — veja [Inadimplência](/modulos/inadimplencia/#enviar-mensagem))
e falhos.

## O que você faz aqui

- **Seleção múltipla** e **exportação em CSV** — do total, dos filtrados pelos cartões ou
  só da seleção.

{: .note }
A exportação traz **uma linha por tentativa de envio**, não só o resumo por ciclo — se um
e-mail foi tentado, falhou e foi reenviado depois, aparecem as duas tentativas
separadamente, cada uma com sua data e seu status.
