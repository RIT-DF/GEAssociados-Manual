---
title: Casos Especiais
parent: Trilha do tesoureiro
nav_order: 4
---

# Casos Especiais

As páginas de [Módulos](/modulos/) explicam cada botão. Aqui é outra coisa: são situações
em que a **ordem** dos passos decide o resultado — fazer a coisa certa na ordem errada
produz um estrago que fazer na ordem certa evita por completo. Cada caso abaixo é a
**decisão** a tomar e a **sequência** a seguir; para o passo a passo de cada tela, os
links levam ao módulo correspondente.

## Família pagou por fora do link enviado

Aconteceu na reunião, por Pix direto, ou em dinheiro — a família pagou, só que não pelo
link que o plugin gerou.

**A decisão:** confirme o pagamento da cobrança. **Nunca cancele** uma cobrança que já foi
paga por fora. Cobrança cancelada some do relatório de recebimentos, do de inadimplência e
da prestação de contas — e o grupo perde o registro de um dinheiro que, de fato, entrou.

**A ordem que evita o estrago:**

1. **Confirme o pagamento da cobrança primeiro** — antes de tocar em qualquer coisa
   relacionada ao pedido do WooCommerce. Use **Confirmar pagamento**, em
   [Detalhe da cobrança](/modulos/cobrancas/#detalhe-da-cobrança) ou em
   [Ações em lote](/modulos/cobrancas/#ações-em-lote).
2. **Registre, na observação da baixa, como a pessoa pagou de fato** — Pix, dinheiro,
   depósito — e **anexe o comprovante**, se houver. É o que vai explicar, meses depois,
   por que aquele pagamento não tem pedido de cartão associado.
3. Só depois disso, se o pedido do WooCommerce vinculado precisar de algum ajuste, mexa
   nele.

{: .important }
**Por que a ordem importa.** Cancelar o pedido do WooCommerce **antes** de confirmar o
pagamento faz o sistema entender que você cancelou a cobrança — porque ela ainda estava
pendente quando o cancelamento chegou. E cobrança cancelada não pode mais ser marcada
como paga: o caminho de confirmação exige uma cobrança pendente. Nessa ordem invertida,
você fica sem conseguir registrar um pagamento que, de fato, aconteceu — e a única saída é
criar uma cobrança avulsa para recuperar o registro, o que seria evitado confirmando na
ordem certa desde o início.

{: .note }
**O princípio por trás disso:** um pagamento que entrou uma vez não pode aparecer duas
vezes na contabilidade do grupo — nem sumir dela. Confirmar antes de mexer no pedido é o
que garante as duas coisas ao mesmo tempo.

## Recibo mostra valor diferente do que a família pagou

Depois de confirmar um pagamento feito por fora (o caso acima), o recibo pode sair com um
valor que não bate exatamente com o que a pessoa transferiu — um real a mais, um a menos.

**Por que acontece:** o recibo mostra o valor **calculado pelo sistema** para aquela data
de pagamento — o mesmo valor que a tela de confirmação usa quando não há um pedido do
WooCommerce para ler o total real. Ele não é o valor que **saiu da conta** de quem pagou;
é a melhor estimativa do sistema para "quanto essa cobrança valia, pago nesse dia".
Divergência de centavos, arredondamento combinado à parte, ou um valor fechado que a
família preferiu pagar — nada disso o sistema tem como saber sozinho.

**O que fazer:**

1. **Explique isso antes que vire reclamação** — é comportamento esperado, não erro do
   sistema. Vale antecipar com quem recebe cobrança por fora com frequência.
2. **Registre a diferença na observação da baixa**, do mesmo jeito que o caso anterior —
   é o que documenta por que o recibo e o extrato do grupo não batem centavo a centavo.
3. **Decidir se há devolução ou cobrança complementar é da tesouraria, não do sistema.**
   O plugin não estorna nem cobra a diferença sozinho — se o grupo decidir ajustar, isso é
   um acerto de contas feito por fora, documentado na observação.

## Importação de planilha com CPF duplicado

A planilha de importação já tem uma proteção própria contra esse erro — ver
[CPF repetido](/modulos/importacao/#cpf-repetido) — e o que cabe aqui é separar o que o
sistema resolve sozinho do que exige decisão sua.

- **O sistema bloqueia sozinho** uma linha cujo CPF já pertence, no arquivo ou no cadastro
  existente, a uma pessoa com **nome diferente** — e bloqueia o grupo familiar inteiro
  daquela linha, não só a pessoa em conflito. Você não precisa fazer nada além de corrigir
  a planilha e reimportar as linhas recusadas.
- **O sistema resolve sozinho, sem avisar**, quando o CPF já existe no cadastro com o
  **mesmo nome** (variação de maiúscula, acento ou espaço não conta como diferença): ele
  reaproveita o cadastro existente em vez de duplicar. Esse é o caminho normal de
  atualizar dado de quem já está no sistema.
- **Exige decisão sua** quando um CPF compartilhado já passou por uma importação
  **antiga**, antes dessa proteção existir, e pode ter fundido duas pessoas por engano. A
  auditoria de CPF (mesma página, seção
  [CPF repetido](/modulos/importacao/#cpf-repetido)) aponta esses casos para você revisar
  — corrigir cadastro fundido por engano é o mesmo procedimento do próximo caso.

## Duas famílias que viraram uma por CPF repetido do responsável

Consequência do caso anterior, quando um CPF de responsável acabou compartilhado por
engano entre duas famílias diferentes: os cadastros se fundem, e uma única cobrança passa
a cobrir jovens de famílias que não têm nada a ver entre si.

**A ordem que separa as famílias sem duplicar cobrança:**

1. **Corrija o cadastro primeiro.** Separe o responsável fundido em dois cadastros
   distintos e recoloque cada jovem na família certa — ver
   [Responsáveis financeiros](/modulos/responsaveis/) e [Famílias](/modulos/familias/).
2. **Cancele a cobrança errada** — a que ainda mistura as duas famílias — em
   [Detalhe da cobrança](/modulos/cobrancas/#detalhe-da-cobrança), com o motivo.
3. **Só então crie as cobranças avulsas**, uma por família, no mesmo ciclo — ver
   [Nova cobrança avulsa](/modulos/cobrancas/#nova-cobrança-avulsa).

{: .important }
**Por que a ordem importa.** O sistema **recusa** criar uma cobrança avulsa para uma
família que já tem, naquele ciclo, uma cobrança **não cancelada** — é a mesma proteção
contra cobrança duplicada que vale em qualquer criação de avulsa. Tentar o passo 3 antes
do passo 2 simplesmente não funciona: a tela recusa e diz que já existe cobrança para
aquele ciclo. Cancelar a cobrança errada é o que abre espaço para as duas novas.

## Um jovem se afastou

Duas ferramentas diferentes decidem o que o jovem **é** no cadastro depois que ele para de
participar — e escolher a errada tem efeito bem diferente.

| Ferramenta | Onde | O que acontece |
|---|---|---|
| **Desativar** | Ação na lista de [Membros](/modulos/membros/) | Sai de tudo: para de ser cobrado, sai da contagem de composição do grupo, some das listas de ativos. Uso: desligamento. |
| **Data de fim de cobrança** | Campo no cadastro do membro, em [Membros](/modulos/membros/) | Continua ativo e visível no sistema — só para de ser cobrado a partir da data informada. Uso: afastamento temporário (licença, viagem longa, pausa combinada). |

**A ordem que evita cobrar quem já saiu:** faça a escolha — desativar ou definir a data de
fim de cobrança — **antes** de gerar a próxima cobrança do grupo, nunca depois. Depois de
gerada, a cobrança já existe com aquele jovem dentro dela: seria preciso desfazer o que já
foi feito, em vez de simplesmente não gerar.

{: .note }
**Documento já emitido não muda.** Uma cobrança guarda os membros que ela cobria no
momento em que foi gerada — desativar alguém depois não reescreve recibo nem declaração
já emitidos com o nome dele. É assim que o histórico do grupo continua batendo com o que
realmente aconteceu em cada mês.

## Cobrança errada num ciclo já gerado

Uma cobrança saiu com valor errado, membro errado, ou qualquer outro problema pontual — e
o ciclo em que ela nasceu já foi gerado inteiro.

**A decisão:** **não regere o ciclo inteiro.** Regerar manda e-mail de novo para todas as
famílias daquele ciclo, inclusive as que não têm nada a ver com o erro — é o jeito mais
rápido de transformar um problema de uma família num incômodo para o grupo inteiro.

**A ordem certa, restrita ao caso específico:**

1. **Cancele só a cobrança com problema**, em
   [Detalhe da cobrança](/modulos/cobrancas/#detalhe-da-cobrança), com o motivo.
2. **Crie uma cobrança avulsa no mesmo ciclo**, para a mesma família ou membro — ver
   [Nova cobrança avulsa](/modulos/cobrancas/#nova-cobrança-avulsa).

{: .warning }
**O valor da avulsa pode não ser igual ao da cobrança cancelada.** Ele vem de um cálculo
**novo**, feito no momento em que você cria a avulsa — nunca copiado do valor da cobrança
anterior. Se alguma regra mudou entre a geração do ciclo e agora, o valor pode ser
diferente, e isso é esperado: é o mesmo motor de cálculo que gera qualquer cobrança normal,
não uma cópia da anterior.
