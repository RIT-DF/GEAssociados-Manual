---
title: Glossário
nav_order: 14
---

# Glossário

Termos do plugin e do mercado de cobrança, explicados do jeito que são usados no
GE Associados — não a definição de dicionário.

**Associado** — no Escotismo, quem tem **registro na União dos Escoteiros do Brasil
(UEB)**: os jovens e os adultos voluntários (escotistas e dirigentes). É o que o plugin
chama de **membro**. Pai, mãe ou tutor que paga a mensalidade **não** é associado nesse
sentido — ver *Associado contribuinte*.

**Associado contribuinte** — quem contribui financeiramente com o grupo sem ter registro
próprio na UEB: tipicamente o pai, a mãe ou o tutor que paga a mensalidade do filho. No
plugin, essa pessoa aparece como **responsável financeiro**, não como membro. A distinção
importa: ela não conta na composição do grupo, não pertence a ramo nem a seção, e não
aparece nos relatórios de associados — mas é quem recebe a cobrança.

**Ciclo de cobrança** — a geração das cobranças de um plano para um período específico
(por exemplo, o ciclo de "mar/2026"). Um plano pode ter vários ciclos ao longo do tempo.

**Cobrança** — o registro de que uma pessoa (ou família) deve um valor num determinado
vencimento. Pode estar pendente, aguardando pedido, vencida, paga, cancelada ou **sem
valor a pagar** (quando o cálculo daquele ciclo fechou em R$ 0,00 — ver
[Cobranças](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)).

**Família** — o grupo de cobrança: reúne um ou dois responsáveis financeiros e os membros
ligados a eles. Não precisa corresponder a uma família no sentido civil — um escotista
adulto pode ficar sem família vinculada.

**Membro** — como o plugin chama o **associado**: um jovem do grupo ou um adulto
voluntário (escotista, dirigente). É quem pertence a um ramo e a uma seção, e quem entra
na contagem de composição do grupo. Diferente do responsável financeiro, que paga sem ser
membro.

**Modo de cobrança** — como a cobrança de um plano é montada: individual (uma cobrança
por membro), familiar (uma cobrança por família) ou híbrido.

**Pedido** — o registro no WooCommerce que carrega o link de pagamento de uma cobrança.
Uma cobrança pode existir sem pedido ainda gerado; o e-mail com o link só sai depois que
o pedido é criado.

**Plano de cobrança** — o que se cobra: nome, valor, frequência e forma de cobrar.
Existe antes de qualquer cobrança individual ser gerada.

**Preset escoteiro** — um conjunto pronto de um plano e três regras (por exemplo,
desconto para irmãos) que o plugin oferece para começar rápido, sem duplicar o que já
existir.

**Regra** — um ajuste automático de valor: desconto, acréscimo, multa, desconto por
antecipação, crédito ou cancelamento, aplicado conforme condições como idade, ramo, seção
ou tamanho da família.

**Responsável financeiro** — a pessoa que recebe e paga a cobrança de uma família. Em
geral é o pai, a mãe ou o tutor — o **associado contribuinte** —, mas pode ser qualquer
pessoa: avó, padrinho, ou o próprio jovem, se for maior de idade. Não precisa ter registro
na UEB e não é contado como associado do grupo.

**Ramo** — a divisão principal do grupo escoteiro (Lobinho, Escoteiro, Sênior, Pioneiro).

**Seção** — o grupo dentro de um ramo (por exemplo, uma alcateia específica dentro do
ramo Lobinho).

**Snapshot de regras** — o retrato congelado das regras vigentes no momento em que uma
cobrança foi emitida. Mudar a regra depois não altera esse retrato.

**Vigência** — o período em que uma versão de regra está em uso para o cálculo de novas
cobranças.
