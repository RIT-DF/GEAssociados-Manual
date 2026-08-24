---
title: Problemas e soluções
nav_order: 8
---

# Problemas e soluções

| Sintoma | Causa provável | O que fazer |
|---|---|---|
| Responsável diz que não recebeu o e-mail de cobrança | Envio automático desligado, cobrança sem pedido gerado, ou e-mail não cadastrado | Veja [Enviar os e-mails de cobrança](/passo-a-passo/enviar-cobrancas/); confira [Entregabilidade](/modulos/entregabilidade/) para o caso específico |
| Nenhum e-mail do plugin está saindo | O e-mail do WordPress não está configurado na hospedagem | Use o **e-mail de teste** em [Diagnóstico](/modulos/diagnostico/); se não chegar, instale um plugin de SMTP |
| Botão "Gerar pedido" apareceu com erro | Falha na comunicação com o WooCommerce, ou cadastro do responsável incompleto | Veja o motivo no acompanhamento do lote; corrija o cadastro e tente de novo pela cobrança individual |
| Valor de uma cobrança não mudou depois de eu editar uma regra | Comportamento esperado: editar regra só afeta cobranças futuras | Para a cobrança já emitida, use **Alterar valor** com o motivo |
| Não consigo excluir um plano de cobrança | O plano já tem um ciclo gerado | Resolva (cancele) as cobranças do ciclo antes de excluir o plano |
| Não consigo cadastrar uma seção num ramo | O ramo está inativo | Reative o ramo em [Ramos e Seções](/modulos/ramos-secoes/) |
| Alguns botões do plugin não aparecem para mim | Seu usuário não tem a permissão correspondente | Peça à coordenação para revisar [Permissões](/modulos/permissoes/) |
| A importação processou algumas linhas e outras não | A importação é parcial por natureza — linha com erro não desfaz as demais | Baixe o CSV de erros, corrija e reimporte só as linhas que faltaram |
| O disparo automático de cobrança parou de funcionar | O segredo do disparo periódico foi trocado, e o agendador externo continua com o antigo | Atualize o agendador externo com o novo segredo, em [Diagnóstico](/modulos/diagnostico/) |
| O responsável esqueceu o link do portal | O link enviado por e-mail expira em 15 minutos | Ele pode pedir um novo link na página do portal, informando o e-mail de novo |
| A sessão do responsável no portal expirou no meio do uso | A sessão dura 4 horas | Ele pede um novo link de acesso, do mesmo jeito que da primeira vez |
| Uma segunda organização não pode ser cadastrada no mesmo site | O plugin atende só uma organização por instalação de WordPress | Para um segundo grupo, use uma instalação separada de WordPress |

{: .note }
Não encontrou o seu caso aqui? Veja o módulo específico em [Módulos](/modulos/) — a
tela costuma explicar o aviso no próprio contexto em que ele aparece.
