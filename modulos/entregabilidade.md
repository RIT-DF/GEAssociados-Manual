---
title: Entregabilidade
parent: Módulos
nav_order: 5
---

# Entregabilidade

**Menu:** Painel e Relatórios → aba Entregabilidade

Mostra, por ciclo de cobrança, se os e-mails realmente chegaram aos responsáveis — e deixa
corrigir e reenviar direto daqui, sem precisar caçar cada caso por fora.

![Relatório de entregabilidade por ciclo, com as sete situações de envio somadas no topo e detalhadas por ciclo na tabela](/assets/img/relatorio-entregabilidade.png)

## Filtros

**Plano, ciclo e período** — o mesmo recorte compartilhado das outras abas de Relatórios
(veja [Painel](/modulos/painel/#o-que-você-vê)): filtrar aqui e trocar de aba mantém a
escolha.

## O que você vê

Por ciclo, cada e-mail cai em uma de sete situações:

| Situação | O que significa | O que fazer |
|---|---|---|
| **Enviado** | Saiu e o servidor aceitou | Nada |
| **Falhou** | O servidor de e-mail recusou | Ver [Diagnóstico](/modulos/diagnostico/) — costuma ser configuração de envio do site |
| **Ignorado** | Descartado de propósito, porque a mesma mensagem já tinha saído hoje | Nada — é proteção contra e-mail repetido, não é erro |
| **Sem destinatário** | Não havia e-mail cadastrado para aquela cobrança | Cadastrar o e-mail do responsável ou do associado |
| **Pedido não gerado** | A cobrança ainda não virou pedido, então não existe link de pagamento | Gerar o pedido em [Cobranças](/modulos/cobrancas/) |
| **Link de pagamento indisponível** | O pedido existe, mas não aceita mais pagamento — já foi concluído ou cancelado direto no WooCommerce | Conferir o status da cobrança; se ainda precisa cobrar, gerar um pedido novo |
| **Lembrete perdido** | O lembrete de atraso não saiu no dia certo, a tentativa de recuperação (até 3 dias) também passou, e o envio automático já não vai mais acontecer para aquela cobrança | Enviar mensagem manualmente — veja [Inadimplência](/modulos/inadimplencia/#enviar-mensagem) |

{: .tip }
Se um responsável reclamar que não recebeu a cobrança, esta é a tela para verificar antes
de qualquer outra coisa. As situações têm causas diferentes e soluções diferentes —
"falhou" é problema de envio do site, "sem destinatário" é cadastro incompleto, "pedido
não gerado" é cobrança que ainda não está pronta para ser paga, "link de pagamento
indisponível" é um pedido que já saiu de circulação, e "lembrete perdido" é um aviso que
não tem mais como sair automaticamente.

{: .important }
**"Pedido não gerado" e "Link de pagamento indisponível" são recuperáveis: resolvido o que
falta (gerar o pedido, gerar um novo link), o próximo envio automático sai normalmente.**
Nos dois casos o lembrete é segurado de propósito — não faria sentido pedir que alguém
pague sem oferecer como, ou oferecer um link que não funciona mais. O financeiro recebe um
aviso por e-mail quando isso acontece, e o Painel também sinaliza.

{: .warning }
**"Lembrete perdido" é diferente: não tem volta.** A rotina diária que dispara os avisos de
atraso tem uma margem de até 3 dias corridos para recuperar um envio que não saiu no dia
exato — por exemplo, se o site ficou fora do ar naquela madrugada. Passados os 3 dias sem
conseguir enviar, o sistema desiste daquele aviso especificamente: ele não sai mais para o
associado, o cadastro não tem nada de errado para corrigir, e a única forma de o
responsável ainda ser avisado é você mandar a mensagem à mão pela Inadimplência. O
financeiro recebe o mesmo aviso consolidado por e-mail sobre esses casos.

## Comunicações com problema

![Lista "Comunicações com problema" sempre visível, com o motivo em linguagem simples e a ação sugerida](/assets/img/entregabilidade-lista-problemas-desktop.png)

![A mesma lista "Comunicações com problema" em celular](/assets/img/entregabilidade-lista-problemas-mobile.png)

Abaixo dos cartões e da tabela por ciclo, a lista **Comunicações com problema** fica
**sempre visível** — antes era preciso clicar num número para descobrir que ela existia.
Cada linha traz o nome, a cobrança, o **e-mail de destino**, o **motivo em linguagem
simples** (não o texto cru que o servidor de e-mail devolveu) e uma **ação sugerida**:
corrigir cadastro, tentar de novo ou enviar manualmente, conforme o caso.

**"Lembrete perdido" entra nessa lista por padrão**, junto com falhou, sem destinatário,
pedido não gerado e link de pagamento indisponível — sem precisar escolher esse filtro. É
a situação mais grave da lista, então ficar escondida atrás de um filtro só faria esconder
o caso que mais precisa de atenção. Na linha, o **e-mail de destino** mostra o endereço que
**teria recebido** o aviso — útil para saber a quem procurar, mesmo sem ter saído e-mail
nenhum — e a **ação sugerida** é "Enviar mensagem manualmente", porque não há cadastro
para corrigir: o e-mail estava certo, o que faltou foi a rotina diária rodar a tempo. O
link da linha abre a cobrança direto, para você registrar o contato ou mandar a mensagem
pela Inadimplência.

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

{: .note }
**"Lembrete perdido" não tem botão de reenviar, nem sozinho nem em lote — de propósito.**
Selecionando esse item numa seleção em lote, ele entra na contagem de "ficará de fora",
com o motivo. O envio automático para aquela cobrança específica não existe mais; o que
resta é mandar a mensagem manualmente pela Inadimplência.

## O que você faz aqui

- **Seleção múltipla** e **exportação em CSV** — do total, dos filtrados pelos cartões ou
  só da seleção.

{: .note }
A exportação traz **uma linha por tentativa de envio**, não só o resumo por ciclo — se um
e-mail foi tentado, falhou e foi reenviado depois, aparecem as duas tentativas
separadamente, cada uma com sua data e seu status.
