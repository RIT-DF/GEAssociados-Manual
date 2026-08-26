---
title: Casos especiais
nav_order: 12
---

# Casos especiais

Situações que fogem do fluxo comum e em que a **ordem dos passos** importa — feito na
ordem errada, o sistema pode registrar algo diferente do que aconteceu de verdade, ou
recusar o próximo passo. Cada caso traz a decisão a tomar e a ordem a seguir; a mecânica
de cada tela está na página do módulo correspondente, linkada em cada passo.

{: .note }
Nem todo grupo passa por todos esses casos — alguns só aparecem quando o grupo integra a
cobrança com outro sistema por fora. O princípio por trás de cada um vale de qualquer
forma: é o que evita o estrago quando a situação aparecer.

## 1. Família pagou por fora do link enviado

Alguém pagou em dinheiro, no Pix direto ou em outro canal que não o link de pagamento que
o sistema enviou.

**Decisão:** confirme a cobrança como **paga** — nunca a cancele. Cancelar diz ao sistema
"não havia nada a pagar aqui": a cobrança some do relatório de
[Recebimentos](/modulos/recebimentos/) e da
[Inadimplência](/modulos/inadimplencia/), e a prestação de contas do mês perde a linha
daquele pagamento. O dinheiro entrou de verdade; o registro precisa refletir isso.

**Ordem a seguir:**

1. **Confirme o pagamento primeiro**, pela cobrança, com a data em que a pessoa pagou de
   fato e o comprovante em anexo (veja [Cobranças](/modulos/cobrancas/#detalhe-da-cobrança)).
2. **Só depois**, se precisar, mexa no pedido correspondente no WooCommerce.

{: .important }
Na ordem inversa — mexer no pedido do WooCommerce antes de confirmar o pagamento no
GE Associados — o sistema entende que **o pedido foi cancelado**, e reflete isso na
cobrança, que ainda estava pendente. Uma cobrança cancelada **não pode mais ser marcada
como paga**. Se isso já aconteceu, você precisa criar uma cobrança avulsa nova para
registrar o pagamento (veja o [caso 6](#6-cobrança-errada-num-ciclo-já-gerado) para o
raciocínio de criar uma avulsa em vez de reabrir a antiga).

Registre, na observação da confirmação de pagamento, **quanto** a pessoa pagou de fato e
**por qual caminho** — é o que faz sentido do valor meses depois, quando ninguém mais
lembra de cabeça.

**Princípio:** um pagamento que entrou uma vez não pode aparecer duas vezes na
contabilidade — nem sumir dela.

## 2. O recibo mostra um valor diferente do que a família pagou

Consequência direta do [caso 1](#1-família-pagou-por-fora-do-link-enviado): o recibo
sempre traz o **valor calculado da cobrança**, não o valor que efetivamente saiu da conta
de quem pagou.

Isso aparece quando alguém pagou por fora com um valor arredondado, combinou um desconto
que não está registrado como regra, ou pagou em mais de uma parcela por fora do sistema.

**O que fazer:** registre a diferença na observação da confirmação de pagamento — o
mesmo campo do [caso 1](#1-família-pagou-por-fora-do-link-enviado). Devolver ou cobrar a
diferença é decisão da tesouraria, não do sistema; o plugin não tem um fluxo para isso
porque a diferença não é uma regra de cálculo, é um acerto combinado fora dele.

## 3. Importação de planilha com CPF duplicado

Uma planilha de importação traz uma linha cujo CPF já pertence, no arquivo ou no cadastro
existente, a uma pessoa com **nome diferente** — sinal comum de erro de digitação no CPF.

**O que o sistema já resolve sozinho:** a importação **recusa** essa linha, e a recusa
**bloqueia o grupo familiar inteiro** daquela linha, não só a pessoa do CPF em conflito —
é a proteção contra criar um cadastro trocado a partir de um dígito errado. Veja
[Importação → CPF repetido](/modulos/importacao/#cpf-repetido).

**O que resolve sozinho, reaproveitando cadastro existente:** quando o CPF é o mesmo e o
nome também bate (ou é reconhecidamente a mesma pessoa), a importação identifica quem já
existe e atualiza o cadastro, em vez de duplicar.

**O que exige decisão sua:** quando o CPF já apareceu em mais de um cadastro de pessoas
diferentes — de uma importação anterior, por exemplo, antes dessa proteção existir — é
você quem decide qual cadastro está certo. Use a **auditoria de CPF** em
[Importação](/modulos/importacao/#cpf-repetido) para encontrar esses casos sem precisar
caçar linha por linha, e corrija o cadastro errado antes de importar de novo.

## 4. Duas famílias que viraram uma por CPF repetido

Quando o [caso 3](#3-importação-de-planilha-com-cpf-duplicado) não foi pego a tempo, dois
cadastros de família podem acabar fundidos por um CPF que, na origem, pertencia a duas
famílias diferentes — e a cobrança gerada passa a cobrir jovens de núcleos familiares que
não têm relação entre si.

**Ordem a seguir:**

1. **Corrija o cadastro primeiro** — separe as famílias em
   [Famílias](/modulos/familias/), com os membros certos em cada uma.
2. **Cancele** a cobrança errada, que ainda mistura as duas famílias.
3. **Só então crie as cobranças avulsas**, uma por família, em
   [Nova cobrança avulsa](/modulos/cobrancas/#nova-cobrança-avulsa).

{: .important }
O sistema **recusa** criar uma cobrança avulsa para uma família enquanto existir, no
mesmo ciclo, uma cobrança não cancelada para ela — é a mesma proteção contra duplicar
cobrança do [caso 6](#6-cobrança-errada-num-ciclo-já-gerado). Por isso o cancelamento
precisa vir **antes** das avulsas, não depois.

## 5. Um jovem se afastou do grupo

Há duas ferramentas para tirar alguém da cobrança, e a escolha muda o que aquele jovem
continua sendo no cadastro — não são intercambiáveis.

| | **Desativar** (em [Membros](/modulos/membros/)) | **Data fim de cobrança** (campo do cadastro) |
|---|---|---|
| O que tira | Cobrança, composição do grupo, contagem de ativos — tudo | Só a cobrança, a partir da data |
| O que preserva | Nada — some de tudo daqui para a frente | Ramo, seção, composição: ele continua ativo e visível |
| Quando usar | Desligamento definitivo do grupo | Afastamento temporário (viagem, licença, pausa) |

**Ordem a seguir:** faça a escolha **antes** de gerar a próxima cobrança do ciclo — se
você desativar ou marcar a data de fim depois que a cobrança já foi gerada, ele entra
nela mesmo assim, porque a geração já congelou quem estava valendo naquele momento.

{: .note }
Documentos já emitidos não mudam de qualquer forma: uma cobrança guarda os membros que
ela cobria **no momento em que foi gerada**, então desativar alguém depois não reescreve
recibo nem declaração já emitidos com o nome dele.

## 6. Cobrança errada num ciclo já gerado

Uma cobrança específica saiu errada dentro de um ciclo que já foi gerado para o grupo
inteiro — um valor calculado errado, uma família que não deveria entrar, um responsável
trocado.

**Decisão:** não regenere o ciclo inteiro. Regenerar reenvia e-mail de cobrança para
**todas** as famílias do ciclo, inclusive as dezenas que não têm nenhuma relação com o
erro — o remédio erra o alvo e ainda cria ruído para quem já estava certo.

**Ordem a seguir:**

1. **Cancele** só a cobrança específica que saiu errada.
2. **Crie uma avulsa** no mesmo ciclo, para a mesma família ou membro — veja
   [Nova cobrança avulsa](/modulos/cobrancas/#nova-cobrança-avulsa).

{: .note }
O valor da avulsa sai de um **cálculo novo**, feito no momento da criação — não é uma
cópia do valor cancelado. Se alguma regra mudou entre a geração do ciclo e agora, o valor
da avulsa pode ser diferente do valor da cobrança que você cancelou. Isso é esperado, não
um sinal de erro.
