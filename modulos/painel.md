---
title: Painel
parent: Módulos
nav_order: 1
---

# Painel

**Menu:** Painel e Relatórios → aba Painel

O painel é o panorama do mês: quanto entrou, quanto ainda é esperado, quem está em
atraso e quais cobranças merecem atenção agora.

![Painel do GE Associados com indicadores do mês e cobranças críticas](/assets/img/painel.png)

![Painel do GE Associados em celular](/assets/img/painel-mobile.png)

## Para que serve

É a primeira tela a olhar quando você quer saber "como estamos indo" sem entrar em cada
relatório separado.

## O que você vê

- **Filtros** por plano, por ciclo e por período — o padrão é o mês corrente. Escolher um
  ciclo trava automaticamente o período e o plano correspondentes a ele. O filtro de
  período recusa uma **data final anterior à inicial** — evita um recorte sem sentido em
  vez de simplesmente devolver vazio.
- **Indicadores**: recebido no mês, previsto até o fim do mês, inadimplência (em valor e
  em percentual), cobranças ativas e taxa de pagamento.
- **Contadores** de membros, famílias e responsáveis ativos, e o **gráfico de 12 meses** —
  esses dois sempre mostram a organização inteira, independentemente do filtro escolhido.
  Isso é proposital: são indicadores de tamanho do grupo, não do recorte que você está
  analisando.
- **Cobranças críticas em aberto**, numa tabela com link direto para cada uma.

{: .tip }
**O recorte que você escolhe aqui vale para as outras abas de Relatórios também.** Filtrou
por um plano e um ciclo no Painel e foi olhar a Inadimplência? A tela já abre com o mesmo
recorte — não precisa escolher de novo. Isso vale trocando entre Painel, Inadimplência,
Recebimentos, Composição e Entregabilidade, e sobrevive a recarregar a página. Antes, cada
aba esquecia o filtro da anterior.

![Painel com um ciclo escolhido: os campos De e Até somem e a tela mostra "Todo o ciclo" no lugar deles](/assets/img/painel-todo-o-ciclo.png)

{: .note }
**Escolheu um ciclo?** Os campos **De** e **Até** ficam vazios e a tela mostra **"Todo o
ciclo"** no lugar deles — o recorte passa a ser o ciclo inteiro, não um intervalo de datas.
Isso vale no Painel e nas demais abas de Relatórios. A exceção é a
[Composição](/modulos/composicao/), que não é sobre cobranças: lá, com um ciclo escolhido,
o período usado é o **mês de vencimento do ciclo**, e a tela avisa isso explicitamente.

{: .note }
**Escolheu um período diferente do mês corrente** (por data ou por ciclo)? Os três
cartões que mudam com o filtro passam a dizer **"Recebido no período"**, **"Previsto até o
fim do período"** e **"Taxa de pagamento do período"**, em vez de "do mês" — para não
sugerir um mês que não é o que está sendo mostrado. Filtrando só por plano, sem mexer no
período, os cartões continuam falando "do mês", porque o servidor mantém o mês corrente
nesse caso.

{: .note }
Contadores e gráfico não mudam com o filtro de plano ou ciclo — só os indicadores
financeiros do topo mudam. Se parecer que o gráfico "não respeitou o filtro", é esse o
motivo, não um erro.

{: .note }
Cobrança **[Sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)** nunca
entra nos indicadores de inadimplência nem nas cobranças críticas — ela não é uma
pendência, é uma cobrança que fechou em R$ 0,00.

## Avisos que podem aparecer

- **Organização não configurada** — falta preencher os dados básicos em
  [Unidade Escoteira](/modulos/unidade-escoteira/).
- **Recorte vazio** — o filtro escolhido não encontrou nenhuma cobrança.
- **Recorte grande demais** — pede para refinar o filtro antes de mostrar o resultado.
- **Cobranças sem link de pagamento** — existem cobranças que ainda não viraram pedido.
  Sem pedido não há link, o responsável não tem como pagar, e o lembrete dele fica
  segurado até o pedido existir (veja
  [Enviar os e-mails de cobrança](/passo-a-passo/enviar-cobrancas/)).
