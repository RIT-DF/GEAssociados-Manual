---
title: Inadimplência
parent: Módulos
nav_order: 2
---

# Inadimplência

**Menu:** Painel e Relatórios → aba Inadimplência

Lista de cobranças em atraso, para a tesouraria priorizar quem cobrar primeiro — e agir
direto na linha, sem precisar abrir a cobrança para cada ação.

![Relatório de inadimplência com valor estimado e faixa de atraso](/assets/img/relatorio-inadimplencia.png)

## Por que isto importa

Cobrar atraso é trabalho repetitivo: identificar quem deve, mandar um lembrete, anotar que
ligou, marcar como paga quando o dinheiro chegar por fora do sistema. Antes, cada um desses
passos exigia abrir a cobrança ou trocar de tela. Agora a lista de inadimplentes é o lugar
onde você faz a rotina inteira — inclusive mandar um texto próprio para uma família, com os
dados da cobrança dela já prontos.

## Filtros

- **Plano, ciclo e período** — o mesmo recorte compartilhado das outras abas de
  Relatórios (veja [Painel](/modulos/painel/#o-que-você-vê)): filtrar aqui e trocar de aba
  mantém a escolha.
- Com um **período** escolhido (por data ou por ciclo), a lista mostra as cobranças **com
  vencimento dentro daquele período que continuam sem pagamento hoje** — não é o histórico
  de quem já esteve em atraso e já pagou depois. Sem período, é toda a inadimplência atual.

## O que você vê

Cada linha traz o **valor atualizado no dia** (não é fixo, porque a multa por atraso muda a
cada dia), os **dias de atraso**, a **faixa de atraso**, o **vencimento**, o **plano**, o
**ciclo**, o **pedido** (o número do pedido WooCommerce), **outras cobranças em aberto**
da mesma família e a **última comunicação enviada**, com o contato usado.

{: .important }
**"Enviado" na última comunicação quer dizer que o servidor aceitou o envio — não que a
família já leu, nem que a mensagem chegou de fato à caixa de entrada.** Para saber se um
envio específico realmente chegou ou falhou, confira em
[Entregabilidade](/modulos/entregabilidade/). Quando a família não tem e-mail cadastrado, a
coluna mostra **"Sem e-mail"** em vez de uma data.

{: .note }
Cobrança **[Sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)** nunca
aparece aqui — ela não está em atraso, está zerada.

## Cobrança de família: uma linha, com detalhe por membro

![Relatório de inadimplência com a linha de uma família expandida, mostrando o valor cobrado e pago de cada membro](/assets/img/relatorio-inadimplencia-agrupado.png)

Quando o atraso é de uma **cobrança familiar**, a linha traz uma seta ao lado do nome do
responsável. Clique para ver quem compõe aquele valor: cada membro, com o quanto foi
cobrado dele. Cobrança de **um membro só** continua linha simples, sem seta.

{: .tip }
Útil na hora de ligar para a família: em vez de "vocês devem R$ 90,00", você já sabe que
são dois jovens, R$ 45,00 cada — e qual dos dois entrou na família depois, se um dos
valores destoar do outro.

## Ações por cobrança

![Linha da lista de inadimplência com as ações disponíveis: enviar mensagem, copiar link, abrir cobrança, abrir família, registrar contato e marcar como paga](/assets/img/inadimplencia-acoes-linha.png)

Cada linha tem, conforme a sua permissão:

- **Enviar mensagem** — abre o modal de mensagem (veja a seção abaixo).
- **Copiar link de pagamento** — cola direto no WhatsApp ou passa de viva voz.
- **Registrar contato** — anota que você ligou, mandou mensagem por fora do sistema ou
  conversou pessoalmente, sem disparar e-mail nenhum. Fica no histórico da cobrança.
- **Marcar como paga** — a mesma ação, com a mesma confirmação, que já existe no detalhe da
  cobrança (veja [Cobranças](/modulos/cobrancas/)).
- **Abrir cobrança** — leva ao detalhe completo.
- **Abrir família** — leva direto ao cadastro da família, **já em modo de edição**, e volta
  para a Inadimplência com o filtro que você tinha ao sair.

{: .note }
Quem só tem permissão de **ver relatórios** enxerga a lista, mas não vê os botões que
mudam alguma coisa (enviar mensagem, registrar contato, marcar como paga, abrir família
para editar). É preciso permissão de **gerir cobranças** — se um botão que você esperava
não aparece, é esse o motivo mais provável.

### Enviar mensagem

![Modal de enviar mensagem aberto, com o menu mostrando as três opções: lembrete de atraso, aviso formal e texto livre](/assets/img/inadimplencia-modal-mensagem.png)

Três opções:

- **Lembrete de atraso** — o modelo que já existe em
  [Comunicação](/modulos/comunicacao/#editar-modelo), com pré-visualização antes de enviar.
- **Aviso formal** — idem, o modelo de cobrança formal.
- **Texto livre** — um texto seu, escrito na hora, para aquela família.

O e-mail sai no mesmo layout dos demais (cabeçalho, rodapé com o contato do financeiro) e
o **link de pagamento da cobrança é anexado automaticamente ao final** — você não precisa
colar o link à mão. O envio fica registrado no histórico da cobrança e aparece em
[Entregabilidade](/modulos/entregabilidade/) como qualquer outro.

{: .important }
**A mesma cobrança não recebe duas comunicações no mesmo dia**, mesmo vindas de fontes
diferentes — um lembrete automático de manhã e uma tentativa de texto livre à tarde, por
exemplo. A segunda tentativa é recusada, com aviso de que já saiu uma comunicação hoje para
aquela cobrança. Em lote, a família cai na contagem de "pulados", não gera erro.

#### O texto livre e as variáveis da cobrança

![Campo de texto livre com a lista de variáveis disponíveis ao lado e a pré-visualização já substituída com os dados da cobrança](/assets/img/inadimplencia-texto-livre-variaveis.png)

Ao lado do campo de texto livre fica a lista das **variáveis disponíveis** — as mesmas que
os modelos de e-mail de [Comunicação](/modulos/comunicacao/#editar-modelo) já usam: nome
curto do responsável, período, vencimento, lista de associados com valores, link de
pagamento, dias em atraso, entre outras. Cada uma mostra, em linguagem simples, o que ela
vira no texto final, com um exemplo.

- **Clique numa variável** da lista para inserir no ponto onde o cursor está.
- A **pré-visualização** mostra o texto já substituído, com os dados reais da cobrança
  escolhida — não um exemplo genérico.
- **Variável escrita errada ou desconhecida** é apontada enquanto você digita, e o botão
  **Enviar** fica desabilitado até corrigir — o sistema nunca manda um `{algo}` cru para a
  família.

  ![Aviso de variável não reconhecida no texto livre, com o botão Enviar desabilitado até a correção](/assets/img/inadimplencia-texto-livre-erro.png)
- Mandando a mesma mensagem para **várias cobranças de uma vez** (envio em lote), cada
  família recebe o texto com os **próprios dados** — o texto é o mesmo, as variáveis não.

{: .tip }
Bom para casos que não cabem num modelo padrão: uma combinação específica com aquela
família, um prazo negociado, uma explicação pontual. Para o que se repete, prefira os
modelos de [Comunicação](/modulos/comunicacao/) — editar um modelo vale para toda cobrança
daquele tipo, o texto livre vale só para aquele envio.

## Ações em lote

![Confirmação de envio em lote, mostrando a quantidade de cobranças selecionadas antes de disparar](/assets/img/inadimplencia-lote-confirmacao.png)

Selecione várias famílias e aplique a mesma ação — enviar mensagem ou reenviar — de uma
vez. Antes de sair, a tela mostra **quantas famílias serão afetadas** e pede confirmação.
Depois de processar, o resultado vem **família por família**: quem recebeu, quem foi
pulado (por exemplo, por já ter recebido uma comunicação hoje) e quem falhou — nunca um
"pronto" genérico que esconde falha parcial.

## O que você faz aqui

- **Seleção múltipla** e **exportação em CSV**, do total ou só da seleção — útil para levar
  a lista para uma reunião de diretoria ou para ligar para os atrasados em ordem.

{: .warning }
Quando a lista é maior do que a tela consegue mostrar de uma vez, o relatório avisa que
truncou o resultado — nesse caso, exporte em CSV para ver a lista completa.

{: .note }
A planilha exportada traz **Plano**, **Período do ciclo** e **Pedido** no fim de cada
linha, depois das colunas que já existiam — a ordem antiga não muda.
