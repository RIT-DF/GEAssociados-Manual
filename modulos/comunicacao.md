---
title: Comunicação
parent: Módulos
nav_order: 17
---

# Comunicação

**Menu:** Configurações → aba Comunicação

Controla os e-mails automáticos: quando saem, o que dizem, e o histórico do que já foi
enviado. Três abas.

## Visão geral

![Aba Visão geral, com envio automático, remetente e tabela de modelos](/assets/img/comunicacao.png)

- **Envio automático** — ligado ou desligado. Desligado, nada sai sozinho; útil para
  revisar modelos antes de ativar de vez.
- **Nome e e-mail do remetente**.
- **Frequência do resumo periódico** — desligado, diário, semanal ou mensal. Sem um
  e-mail financeiro cadastrado (veja [Unidade Escoteira](/modulos/unidade-escoteira/)),
  nenhum resumo sai, e a tela avisa disso.
- Tabela de **modelos** e **envios recentes**.

{: .important }
**Se o remetente configurado aqui não é o que realmente sai no e-mail**, esta aba e o
[Diagnóstico](/modulos/diagnostico/#remetente-divergente) avisam. Acontece quando outro
plugin ou o próprio servidor de e-mail troca o remetente por conta própria — o campo
continua certo aqui, mas o responsável recebe de outro endereço, o que pode fazer o
e-mail cair em spam ou parecer suspeito.

## Editar modelo

![Edição de um modelo de e-mail, com marcadores](/assets/img/comunicacao-modelo.png)

Assunto, **dias em relação ao vencimento** (número negativo dispara antes do vencimento),
corpo em HTML (editor visual ou código) e corpo em texto puro, editados à parte. Use
**marcadores** como `{member_name}` para inserir dados de cada cobrança automaticamente.
Há **pré-visualização** sem salvar, e a opção de **restaurar o padrão**.

## Cobrança sem valor a pagar

![Aba Visão geral com a linha do modelo "Cobrança sem valor a pagar" na tabela de modelos](/assets/img/comunicacao-modelo-sem-valor.png)

Quando uma cobrança fica **[Sem valor a pagar](/modulos/cobrancas/#cobrança-sem-valor-a-pagar)**,
ela não entra na sequência normal de lembretes — em vez disso dispara o modelo
**Cobrança sem valor a pagar**, editável como qualquer outro, com assunto padrão
`{periodo}: nada a pagar`.

Esse e-mail é diferente dos demais em três pontos:

- sai **uma única vez** por cobrança, não numa sequência de dias antes/depois do
  vencimento;
- **não tem link de pagamento** — não haveria o que pagar;
- usa o marcador `{motivo_zerado}`, que insere **qual regra** zerou o valor daquela
  cobrança específica. É o que permite ao responsável entender a isenção em vez de
  só receber um "R$ 0,00" sem explicação — e contestar, se achar que a regra não deveria
  valer para o caso dele.

{: .note }
`{motivo_zerado}` só faz sentido nesse modelo. Usado em qualquer outro, ele aparece em
branco — o marcador não inventa um motivo para uma cobrança que não está zerada.

## O e-mail que o responsável recebe

<!-- CAPTURA PENDENTE: comunicacao-email-familia (desktop) — e-mail de
     cobrança de uma família, mostrando a lista de membros. Não capturado
     nesta sessão: não havia, no WordPress local, uma cobrança familiar com
     e-mail já disparado no Mailpit — só cobranças individuais e reenvios
     manuais. Recapturar quando houver um ciclo com família cobrada. -->

O e-mail de cobrança traz o botão **Pagar agora**, e — logo abaixo, por escrito — o mesmo
endereço, para quem usa um cliente de e-mail que não exibe botões corretamente. O botão
sai na cor cadastrada da sua organização (veja
[Unidade Escoteira](/modulos/unidade-escoteira/)), sempre com contraste suficiente para o
texto continuar legível — se a cor escolhida for clara demais, o sistema ajusta o texto do
botão para continuar visível, sem que você precise pensar em combinação de cores.

Numa cobrança de **família**, o e-mail lista quem compõe o valor: o nome de cada membro e
quanto ele representa no total. É o mesmo princípio de minimização de sempre — só nome e
valor, sem CPF, data de nascimento ou qualquer outro dado.

{: .note }
Essa lista aparece mesmo em instalações que já tinham o plugin antes dessa mudança — não é
preciso reeditar nenhum modelo de e-mail para ela funcionar.

### Confirmação de pagamento traz o link do recibo

O e-mail de **Pagamento confirmado** ganhou, no fim do corpo, o link **Baixar recibo** —
leva direto para o [portal do responsável](/responsavel/portal/#o-que-você-vê-ao-entrar).
Veja o comportamento de quem clica sem sessão aberta em
[Documentos](/responsavel/portal/#documentos).

### Contato do financeiro no rodapé

<!-- CAPTURA PENDENTE: comunicacao-rodape-contato (desktop) — o rodapé de um
     e-mail de cobrança, mostrando o contato do financeiro. Não capturado
     nesta sessão: agente em background, sem sessão autenticada — o login é
     do usuário. -->

Todo e-mail que o plugin manda — cobrança, lembrete, resumo periódico, cobrança sem valor
a pagar — traz, no rodapé, o **contato do financeiro** do grupo. Quem responder a
mensagem cai direto nesse endereço, em vez de esbarrar num "não responda" sem saída.

O endereço vem do **e-mail financeiro** cadastrado em
[Unidade Escoteira](/modulos/unidade-escoteira/) — o mesmo que recebe o resumo
periódico. Sem esse campo preenchido, o rodapé usa o remetente configurado em
Comunicação.

## Histórico

![Aba de histórico de envios](/assets/img/comunicacao-historico.png)

Filtros por status e período. Cada linha mostra quando, o evento, os dias em relação ao
vencimento, o destinatário, a cobrança relacionada, o status do envio e o erro, se houver.

{: .tip }
Se um responsável reclamar que não recebeu um e-mail, esta aba costuma responder mais
rápido que investigar por fora — busque pelo nome dele e veja o status exato daquele
envio.

### Reenviar um envio

<!-- CAPTURA PENDENTE: comunicacao-reenviar (desktop) — a linha de um envio
     falho no histórico, com a ação Reenviar disponível, e a barra de ações
     em lote. Não capturado nesta sessão: agente em background, sem sessão
     autenticada — o login é do usuário. -->

Envio que falhou pode ser reenviado direto daqui — por linha ou em lote, selecionando
várias de uma vez.

- **Reenviar algo que já deu certo** pede confirmação: o sistema pergunta antes, porque
  reenviar um e-mail que o responsável já recebeu manda uma segunda cópia, o que confunde
  mais do que ajuda.
- **Item "sem destinatário"** não tem para onde reenviar — o link leva direto ao cadastro
  do responsável ou do membro, para você completar o e-mail e resolver na origem antes de
  tentar de novo.
