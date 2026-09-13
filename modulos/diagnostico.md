---
title: Diagnóstico
parent: Módulos
nav_order: 22
---

# Diagnóstico

**Menu:** Configurações → aba Diagnóstico

Confere se o plugin está funcionando como deveria, e ajuda a resolver quando não está.

![Tela de diagnóstico com lista de verificações](/assets/img/diagnostico.png)

![Tela de diagnóstico em celular](/assets/img/diagnostico-mobile.png)

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

## Logo dos documentos sem aparecer

Outra verificação confere se a logo do grupo e a marca do GE Associados foram desenhadas
com sucesso no último recibo ou declaração gerados. Quando o arquivo cadastrado não pôde
ser lido — corrompido, ou num formato que o gerador de PDF não entende (só JPEG e PNG) —,
o documento sai sem aquela imagem, e o Diagnóstico avisa aqui, dizendo qual das duas
falhou e por quê.

{: .note }
O documento **não deixa de ser gerado** por causa disso — recibo sem logo é melhor que
recibo que não sai. Se o problema é na **logo do grupo**, recadastre o arquivo em
[Unidade Escoteira](/modulos/unidade-escoteira/) e o aviso some sozinho. Se for na **marca
do GE Associados** do rodapé, não há nada para você recadastrar — ela é um arquivo interno
do plugin; fale com o suporte técnico ([Enviar feedback](/modulos/feedback/)) se esse aviso
específico aparecer.

## Converter o controle de permissões

A partir da v1.80.0, o GE Associados pode passar a resolver permissões do mesmo jeito que
os demais plugins da mesma família (instalados no mesmo site, se o grupo usar mais de
um). É essa conversão que esta seção faz — e, enquanto você não clicar em nada aqui,
**nada muda para ninguém**: as telas do plugin mostram só um aviso lembrando que a mudança
existe, com um atalho de volta para cá.

### Por que fazer

Hoje, cada plugin decide sozinho quem pode acessá-lo. Depois da conversão, o GE
Associados passa a usar o mesmo motor que os outros — então dar ou tirar acesso de alguém
à tesouraria passa a funcionar do mesmo jeito em todos os plugins que essa pessoa usa, em
vez de um comportamento diferente em cada um.

### Antes de converter

A conversão só entende dois papéis: quem já **administra o site inteiro**, e quem tem o
papel **Tesoureiro (GE Associados)**. Se hoje alguém acessa o GE Associados por um
**terceiro papel** — Editor, Colaborador, ou um papel personalizado que o grupo tenha
criado e marcado na tela de [Permissões](/modulos/permissoes/) — essa pessoa **perderia
acesso** na conversão, e por isso a conversão **recusa** rodar enquanto ela não for
resolvida. Resolva de um dos dois jeitos, antes de tentar de novo:

- dê a essa pessoa o papel **Tesoureiro (GE Associados)**, na tela de Usuários do
  WordPress; ou
- tire dela a permissão do GE Associados, se o acesso não for mais necessário.

### O ensaio a seco

Antes de converter de verdade, a tela simula o resultado, pessoa a pessoa, sem alterar
nada:

![Ensaio a seco da conversão de permissões, com a tabela por pessoa e o botão Converter agora](/assets/img/diagnostico-conversao-ensaio.png)

Cada pessoa com alguma permissão do GE Associados hoje aparece numa tabela com o que ela
tem **hoje**, o que passaria a ter **depois da conversão**, e um veredito: **Igual**,
**Ganha acesso** (normalmente porque a pessoa já administra o site inteiro) ou **Perde
acesso**. Havendo alguém no veredito **Perde acesso**, o botão de converter fica
indisponível até você resolver o caso dela, como descrito acima.

### Convertendo

Com o ensaio limpo (ninguém perde acesso), o botão **Converter agora** libera. Ele pede
confirmação dizendo **quantas pessoas serão convertidas** — a mesma contagem do ensaio:

![Confirmação da conversão, dizendo quantas pessoas serão convertidas](/assets/img/diagnostico-conversao-confirmacao.png)

{: .important }
A conversão não tem desfazer pela tela. Se o grupo usa papéis personalizados para o GE
Associados hoje, resolva-os antes (seção acima) — depois de converter, só Administrador e
Tesoureiro contam.

Depois de confirmar, a tela mostra **"Conversão feita em"**, com data e hora, e o mesmo
registro por pessoa, agora como **antes/depois** — útil para conferir depois, ou para
mostrar a quem perguntar por que o acesso de alguém mudou:

![Diagnóstico depois da conversão, com o registro antes e depois por pessoa](/assets/img/diagnostico-conversao-feita.png)

### O que muda na tela de Permissões

Depois de converter, a tela [Permissões](/modulos/permissoes/) passa a funcionar de um
jeito mais simples — veja o detalhe lá.
