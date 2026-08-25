---
title: Novidades
nav_order: 11
---

# Novidades

Um resumo, em linguagem simples, do que mudou nas versões mais recentes — o que interessa
para quem usa o plugin no dia a dia, não o registro técnico completo.

## Copiar link de pagamento direto do detalhe da cobrança

O detalhe de uma cobrança pendente com pedido válido ganhou o botão **Copiar link de
pagamento** — cola direto no WhatsApp ou passa de viva voz, sem precisar esperar o próximo
e-mail automático. Veja [Cobranças](/modulos/cobrancas/#copiar-link-de-pagamento).

## Marcar pedido como pago no WooCommerce agora dá baixa sozinho

Antes, marcar um pedido como Concluído ou Processando direto no WooCommerce não refletia
na cobrança — ela continuava Pendente até alguém confirmar o pagamento manualmente aqui.
Agora a baixa acontece sozinha. Vale só para pedidos alterados **depois** dessa
atualização; o que já tinha sido concluído manualmente antes continua exigindo baixa
manual. Veja [A rotina do mês](/tesoureiro/rotina-mensal/#5-dar-baixa-no-que-entrou-por-fora).

## E-mail de cobrança mostra quem compõe o valor da família

Numa cobrança de família, o e-mail passou a listar o nome e o valor de cada membro que
compõe o total — sem outros dados pessoais. O botão **Pagar agora** também passou a sair
sempre com contraste garantido, na cor da organização. Veja
[Comunicação](/modulos/comunicacao/#o-e-mail-que-o-responsável-recebe).

## A lista de importações mostra o nome do arquivo e quanto entrou

A lista de importações passou a mostrar o **nome do arquivo como você enviou** e uma
coluna **Resultado**, com quantos registros entraram e quantos deram erro. O botão **Ver**
agora leva ao lugar certo: o relatório completo numa importação já processada, ou a
pré-visualização numa que ainda está aguardando. E o CSV de erros pode ser baixado a
qualquer momento — não só logo depois de importar —, então dá para corrigir a planilha
com calma e reimportar só as linhas que faltaram. Veja
[Importar dados de uma planilha](/passo-a-passo/importar-dados/).

## Ramo e seção que ainda não existem se resolvem na hora, na importação

Antes, importar uma planilha exigia que os ramos e seções já estivessem cadastrados com o
nome exato usado nela — senão a maioria das linhas dava erro. Agora, quando a planilha traz
um valor que ainda não existe, aparece um passo próprio listando cada um, com quantos
associados estão atrás dele, para você escolher entre vincular a um ramo ou seção já
cadastrado ou criar um novo. Nada é criado automaticamente. Veja
[Importar dados de uma planilha](/passo-a-passo/importar-dados/).

## Importação aceita datas escritas de mais jeitos

A importação de planilha passou a aceitar dia e mês com um dígito só e os separadores `/`,
`-` e `.`. Nas colunas de data de ingresso e de fim de cobrança, também dá para informar
só o ano ou mês e ano — o sistema completa para o primeiro dia do período. Data de
nascimento continua exigindo o dia completo, porque é ela que define a categoria e o
valor cobrado. Veja [Importar dados de uma planilha](/passo-a-passo/importar-dados/).

## Colunas repetidas na planilha não se perdem mais

Planilha com duas colunas de mesmo nome (duas "Observações", por exemplo) antes perdia
uma delas em silêncio na importação. Agora as duas aparecem no mapeamento, com aviso de
que o nome se repete, e cada uma pode ser mapeada para um campo diferente. Veja
[Importar dados de uma planilha](/passo-a-passo/importar-dados/).

## Cabeçalho da planilha não precisa mais ser a primeira linha

Planilha com um título, um logo ou uma nota acima da tabela de dados antes confundia a
importação, sem avisar. Agora o sistema procura em qual linha estão os nomes das colunas,
diz qual usou e deixa escolher outra se precisar. Veja
[Importar dados de uma planilha](/passo-a-passo/importar-dados/).

## Nova aba Shortcodes, e o Portal do Responsável ganha atributos

Configurações ganhou a aba **Shortcodes**, que mostra o código de cada página que o
plugin publica (`[gea_portal]` e `[gea_simulador]`), para quem é cada uma e o estado da
página — inclusive um jeito de recriar a página se ela foi apagada por engano. Veja
[Shortcodes](/modulos/shortcodes/).

O `[gea_portal]` também passou a aceitar seis atributos opcionais — título, quais
cobranças aparecem, card de contato, histórico de acessos, seção de documentos e um
limite de itens — para montar a página do jeito que o grupo preferir. Sem usar nenhum,
a página continua exatamente como sempre foi.

## Recibo e declaração anual no portal do responsável

O portal do responsável ganhou uma seção **Documentos**: o link **Baixar recibo** ao lado
de cada pagamento na lista "Pago", e o botão **Baixar declaração anual**, com tudo que foi
pago no ano num único PDF. São documentos informais, sem valor fiscal. Veja
[Acompanhar e pagar as cobranças](/responsavel/portal/).

## Cobrança em aberto agora indica como resolver

No portal do responsável, cada cobrança em aberto passou a terminar num caminho claro: o
link **Pagar agora**, quando já existe pedido para pagar, ou a orientação para procurar a
diretoria do grupo, quando ainda não existe. O termo "diretoria do grupo" é um rótulo
configurável em [Rótulos](/modulos/rotulos/). Veja
[Acompanhar e pagar as cobranças](/responsavel/portal/).

## Enviar Feedback ganhou tipo, anexos e cópia por e-mail

O formulário de **Enviar Feedback**, no cabeçalho de qualquer tela, agora deixa escolher
o tipo (sugestão, dúvida, bug, depoimento ou outros), anexar arquivos (até 5, 5 MB cada) e
optar por incluir os dados da organização para agilizar o atendimento. Quem envia recebe
uma cópia da mensagem por e-mail. Veja [Enviar feedback](/modulos/feedback/).

## Status da importação em português

A lista de importações passou a mostrar o status de cada uma em português — Concluída,
Falhou, Aguardando processamento — em vez do termo em inglês.

## Botão de escolher arquivo ficou mais claro

Nas telas onde se envia um arquivo — importação de planilha, importação de configuração e
comprovante de pagamento —, o controle cinza do navegador deu lugar a um botão com rótulo
próprio, mais fácil de identificar.

## Vencimento passa a considerar o dia inteiro

A comparação de vencimento agora olha para o **dia**, não para um horário exato. Antes,
dependendo da hora em que a cobrança era conferida, ela podia aparecer como vencida
algumas horas antes ou depois da meia-noite local — o que também afetava o cálculo de
multa por atraso e o número de dias mostrado no e-mail. Agora a virada acontece
exatamente à meia-noite no fuso da sua organização.

## Importação de planilha ganha segundo responsável e "quem paga"

O modelo de planilha para importar membros e famílias passou a aceitar um **segundo
responsável financeiro** e uma coluna para dizer **quem paga** (o primeiro, o segundo,
ambos ou nenhum). Planilhas antigas, sem essas colunas, continuam funcionando exatamente
como antes.

## Painel com filtro por plano, período e ciclo

O Painel deixou de mostrar só o total geral: agora dá para filtrar por plano de cobrança,
por período de datas ou por ciclo específico — útil para conferir só uma turma, um mês ou
um ciclo isoladamente.

## Relatórios de composição e entregabilidade

Dois relatórios novos: **Composição**, que mostra quem está ativo por ramo e seção, com
entradas e saídas — voltado para a coordenação e a diretoria; e **Entregabilidade**, que
mostra se os e-mails de cobrança realmente chegaram, por ciclo.

## Relatórios de inadimplência e recebimentos

Dois relatórios novos: **Inadimplência**, mostrando há quanto tempo cada cobrança está em
aberto; e **Recebimentos**, com tudo que entrou no período. Também foi adicionado um campo
de método de pagamento em cada cobrança.

## Portal do responsável, sem precisar de usuário e senha

Responsáveis financeiros e membros que não têm conta no site agora podem acessar um
portal próprio ("Minhas Cobranças") pedindo um link de acesso por e-mail — sem precisar
de usuário e senha do WordPress. O portal mostra as cobranças pagas e em aberto, os
acessos recentes à conta e permite atualizar dados de contato.

## Simulador público de valores

Qualquer visitante do site pode simular quanto pagaria antes de se inscrever no grupo,
numa página pública. O simulador só aparece quando algum plano de cobrança estiver
marcado como "valor divulgado".

## CNPJ com letras e busca de endereço por CEP

O campo de CNPJ passou a aceitar o novo formato alfanumérico da Receita Federal. E o
cadastro da organização agora busca o endereço automaticamente a partir do CEP,
preenchendo só os campos que estiverem vazios.

{: .note }
Para o histórico técnico completo, o desenvolvedor mantém o registro de mudanças no
repositório do código.
