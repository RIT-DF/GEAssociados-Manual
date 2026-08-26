---
title: Diagnóstico
parent: Módulos
nav_order: 22
---

# Diagnóstico

**Menu:** Configurações → aba Diagnóstico

Confere se o plugin está funcionando como deveria, e ajuda a resolver quando não está.

![Tela de diagnóstico com lista de verificações](/assets/img/diagnostico.png)

## O que você encontra

- **Lista de verificações**, cada uma com a situação atual e uma explicação em português
  de gente.
- **Envio de e-mail de teste** para um endereço que você digitar — a forma mais rápida de
  confirmar que o site consegue mandar e-mail antes de depender disso para cobrar de
  verdade (veja [Antes de instalar → Envio de e-mail](/antes-de-instalar/#envio-de-e-mail)).
- **Avisos dispensados** — os que você já leu e marcou como resolvidos podem ser
  reativados aqui, se precisar revê-los.
- **Disparo periódico** — mostra o último disparo, com IP e hora, e permite **trocar o
  segredo** usado para autenticar o disparo automático por agendador externo.

{: .warning }
Trocar o segredo do disparo periódico **quebra qualquer agendador externo já configurado**
com o segredo antigo — se o grupo usa um serviço externo para disparar as cobranças
automaticamente, atualize-o com o novo segredo assim que trocar, ou o disparo para de
funcionar sem aviso.

## Remetente divergente

<!-- CAPTURA PENDENTE: diagnostico-remetente-divergente (desktop) — a
     verificação de remetente na lista, no estado de aviso. Não capturado
     nesta sessão: agente em background, sem sessão autenticada — o login
     é do usuário. -->

Uma das verificações da lista compara o remetente configurado em
[Comunicação](/modulos/comunicacao/) com o que realmente sai no e-mail. Quando os dois
divergem, o Diagnóstico avisa aqui.

Não é erro do plugin: costuma ser **outro plugin instalado no site**, ou o próprio
**servidor de e-mail**, trocando o remetente por conta própria antes do envio. O campo em
Comunicação continua correto — o problema está em outra camada. Vale revisar a
configuração de SMTP do site quando esse aviso aparecer.
