---
title: Importar dados de uma planilha
parent: Passo a passo
nav_order: 4
---

# Importar dados de uma planilha

## Por que isto importa

Se o grupo já mantém os associados numa planilha, cadastrar um por um no plugin é
desperdício de tempo. A importação lê a planilha e cria os membros, famílias e
responsáveis de uma vez — e é tolerante a erro: uma linha com problema não desfaz as
demais.

## Passo a passo

1. Abra **Famílias e Membros → Importação**.
2. Envie o arquivo — **XLSX ou CSV**, até **5 MB** e **1000 linhas**, com a primeira linha
   sendo o cabeçalho.
3. Confira a **prévia** das primeiras linhas.
4. No **mapeamento de colunas**, revise o que o sistema já adivinhou sozinho — dá para
   corrigir uma coluna mapeada errada ou marcar uma coluna para **ignorar**.
5. Escolha a **política de sobrescrita**:
   - **Ignorar existentes** — quem já está cadastrado não é tocado.
   - **Preencher só campos vazios** — completa o que falta, sem sobrescrever o que já
     existe.
   - **Sobrescrever tudo** — troca os dados existentes pelos da planilha (o sistema mostra
     uma prévia do que vai mudar antes de aplicar).
6. Clique em **Processar** e acompanhe o relatório.

{: .note }
O sistema identifica quem já existe por **CPF** ou, na falta dele, por **nome completo
mais data de nascimento**. Duas pessoas homônimas, nascidas no mesmo dia e sem CPF
cadastrado, são tratadas como a mesma pessoa — vale conferir o resultado quando o grupo
tiver esse caso.

## Exemplo

O Grupo Trilha Verde tem uma planilha com 180 famílias, herdada de anos de controle
manual. Na primeira importação, a tesouraria escolhe **Ignorar existentes** — como é a
primeira vez, não há ninguém cadastrado ainda, então todo mundo entra. Três meses depois,
ao atualizar telefones e e-mails que mudaram, a tesouraria reimporta a mesma planilha
atualizada com a política **Preencher só campos vazios** — mantendo os dados que já foram
ajustados manualmente dentro do plugin.

## O que pode dar errado

- **Algumas linhas deram erro** — a importação é parcial: as linhas sem erro são
  processadas normalmente, e a lista de erros sai em um arquivo CSV para você corrigir e
  reimportar só o que faltou.
- **Coluna obrigatória sem mapear** — o sistema tenta adivinhar pelo nome da coluna na
  planilha, mas nem sempre acerta; confira o mapeamento antes de processar, especialmente
  se a planilha usa nomes de coluna fora do padrão.
- **Arquivo maior que 5 MB ou 1000 linhas** — divida a planilha em partes menores e
  importe uma de cada vez.

## Depois de importar

A lista de importações (na mesma tela) permite ver o resultado de cada uma, arquivar e
desarquivar, inclusive em lote — útil para manter só as importações recentes visíveis no
dia a dia.
