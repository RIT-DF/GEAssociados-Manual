---
title: Permissões
parent: Módulos
nav_order: 18
---

# Permissões

**Menu:** Configurações → aba Permissões

Uma matriz que cruza os papéis de usuário do WordPress com o que cada um pode fazer
dentro do plugin. O que você vê aqui muda depois que o grupo faz a
[conversão de permissões](/modulos/diagnostico/#converter-o-controle-de-permissões), em
[Diagnóstico](/modulos/diagnostico/) — as duas situações estão descritas abaixo.

![Tela de permissões, matriz de papéis por capacidade](/assets/img/permissoes.png)

![Tela de permissões em celular](/assets/img/permissoes-mobile.png)

## Antes da conversão

Quem já administra o site inteiro aparece com tudo marcado e travado — não dá para tirar
permissão de administrador por aqui. Para os demais papéis (editor, colaborador, ou
papéis personalizados que o grupo tenha criado), marque o que cada um pode acessar dentro
do GE Associados.

{: .tip }
Use esta tela para dar acesso ao plugin a alguém da tesouraria ou da coordenação **sem**
precisar compartilhar a senha de administrador do site. Veja também
[Configurações adicionais → Permissões](/configuracoes-adicionais/#permissões).

## Depois da conversão

![Tela de permissões depois da conversão, só com Administrador e Tesoureiro](/assets/img/permissoes-depois-conversao.png)

![Tela de permissões depois da conversão, em celular](/assets/img/permissoes-depois-conversao-mobile.png)

A tela fica mais simples: só existem duas linhas, **Administrador** (travada, sempre com
tudo marcado) e **Tesoureiro (GE Associados)** — é nela que você marca o que o Tesoureiro
pode fazer dentro do plugin. Nenhum outro papel do site — Editor, Colaborador, ou um papel
personalizado do grupo — concede mais nenhum acesso ao GE Associados, mesmo que ainda
apareça marcado em outro lugar.

{: .note }
**Quem é Tesoureiro não se decide mais aqui.** Isso passou a ser função da tela **Usuários**
do próprio WordPress: para dar a alguém acesso de Tesoureiro, edite o usuário dela lá e
escolha o papel **Tesoureiro (GE Associados)**. Esta tela continua sendo o lugar de decidir
**o que** o Tesoureiro pode fazer — só deixou de decidir **quem** é o Tesoureiro.

{: .tip }
Quem já administra o site inteiro continua com acesso total ao GE Associados, sem precisar
de papel nenhum extra — a mesma regra de sempre.
