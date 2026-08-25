---
title: Novidades
nav_order: 11
---

# Novidades

Um resumo, em linguagem simples, do que mudou nas versões mais recentes — o que interessa
para quem usa o plugin no dia a dia, não o registro técnico completo.

## Enviar Feedback ganhou tipo, anexos e cópia por e-mail

O formulário de **Enviar Feedback**, no cabeçalho de qualquer tela, agora deixa escolher
o tipo (sugestão, dúvida, bug, depoimento ou outros), anexar arquivos (até 5, 5 MB cada) e
optar por incluir os dados da organização para agilizar o atendimento. Quem envia recebe
uma cópia da mensagem por e-mail. Veja [Enviar feedback](/modulos/feedback/).

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
