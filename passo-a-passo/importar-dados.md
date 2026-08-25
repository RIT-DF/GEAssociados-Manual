---
title: Importar dados de uma planilha
parent: Passo a passo
nav_order: 4
---

# Importar dados de uma planilha

{: .important }
**Envie um arquivo com apenas a aba de dados.** O sistema lê a **primeira aba visível**
da planilha — abas ocultas são ignoradas. Se a sua planilha de trabalho tem, antes da aba
de dados, outra aba visível (uma capa, um resumo, um controle), é ela que vai ser lida, e
não a sua. O resultado não dá erro: aparece uma pré-visualização com poucas linhas e
nomes que você não reconhece — dado plausível, mas errado. Se o arquivo não tiver
nenhuma aba visível, o envio é recusado, pedindo para deixar a aba de dados visível antes
de reenviar.

{: .tip }
No LibreOffice ou no Excel, clique com o botão direito na aba de dados → **Mover ou copiar
planilha** → *Copiar* → destino **novo documento**. Você fica com um arquivo de uma aba só
para enviar, e a planilha de trabalho do grupo continua intacta.

## Por que isto importa

Se o grupo já mantém os associados numa planilha, cadastrar um por um no plugin é
desperdício de tempo. A importação lê a planilha e cria os membros, famílias e
responsáveis de uma vez — e é tolerante a erro: uma linha com problema não desfaz as
demais.

## Passo a passo

1. Abra **Famílias e Membros → Importação**.
2. Envie o arquivo — **XLSX ou CSV**, até **5 MB** e **1000 linhas**. O sistema procura
   sozinho em qual linha estão os nomes das colunas — não precisa ser a primeira — e avisa
   qual usou, por exemplo "Os nomes das colunas foram encontrados na linha 3. As linhas
   acima foram ignoradas." Se sua planilha tem um título, um logo ou uma nota acima da
   tabela de dados, isso deixou de ser problema: as linhas acima do cabeçalho não viram
   associados. Errou a linha? Dá para escolher outra.
3. Confira a **prévia** das primeiras linhas: o número de linhas bate com o tamanho da
   sua base, e os nomes das colunas são os que você espera? Esse é o momento de pegar
   uma aba errada lida por engano, ou um cabeçalho identificado na linha errada — depois
   disso, o dado errado já pode ter entrado no sistema.
4. No **mapeamento de colunas**, revise o que o sistema já adivinhou sozinho — dá para
   corrigir uma coluna mapeada errada ou marcar uma coluna para **ignorar**. Se a planilha
   tiver duas colunas com o mesmo nome (duas "Observações", por exemplo), o sistema avisa
   quantas vezes o cabeçalho se repete e deixa mapear cada uma para um campo diferente —
   antes, a segunda simplesmente desaparecia.
5. **Se a planilha usar nomes de ramo ou seção que ainda não existem no sistema**, aparece
   um passo próprio antes do processamento.

   ![Passo de ramo e seção: cada valor novo com a contagem de associados e a escolha entre vincular a um existente ou criar](/assets/img/importacao-ramo-secao.png)

   Para cada valor novo, escolha:
   - **Vincular a um já cadastrado** — quando o nome da planilha é só uma grafia diferente
     de um ramo ou seção que já existe ("Alcateia Lua" na planilha, "Alcateia da Lua" no
     sistema).
   - **Criar** — quando é mesmo um ramo ou seção novo. O nome vem preenchido com a grafia
     mais comum encontrada na planilha, e dá para editar antes de aplicar.

   Esse passo só aparece quando há valor novo; planilha cujos ramos e seções já existem
   todos não passa por ele. Variações de maiúscula, acento e espaço em um mesmo nome são
   agrupadas como um item só.

   {: .tip }
   Ao lado de cada valor novo aparece **quantos associados estão atrás dele** — é a pista
   mais confiável de erro de digitação. Se "Alcateia Lua" tem 43 associados e "Alcateia
   Lu" tem 1, o segundo quase sempre é erro de digitação na planilha, não um ramo
   diferente de verdade. Vincule o de contagem baixa ao correto em vez de criar um novo.

   {: .warning }
   Ramo e seção **nunca** são criados sozinhos: a decisão é sempre sua, neste passo. Se
   você vincular errado, a família ou o membro entra no ramo ou seção que você escolheu —
   confira antes de aplicar.
6. Escolha a **política de sobrescrita**:
   - **Ignorar existentes** — quem já está cadastrado não é tocado.
   - **Preencher só campos vazios** — completa o que falta, sem sobrescrever o que já
     existe.
   - **Sobrescrever tudo** — troca os dados existentes pelos da planilha (o sistema mostra
     uma prévia do que vai mudar antes de aplicar).
7. Clique em **Processar** e acompanhe o relatório.

{: .note }
O sistema identifica quem já existe por **CPF** ou, na falta dele, por **nome completo
mais data de nascimento**. Duas pessoas homônimas, nascidas no mesmo dia e sem CPF
cadastrado, são tratadas como a mesma pessoa — vale conferir o resultado quando o grupo
tiver esse caso.

{: .note }
As datas aceitam dia e mês com um dígito só (5/12/2018, 1/1/2020) e os separadores `/`,
`-` e `.`. Nas colunas **Data de ingresso** e **Data fim de cobrança**, também dá para
informar só o ano (2018) ou mês e ano (12/2018) — o sistema completa para o primeiro dia
do período e avisa, ao final do processamento, quantas datas foram completadas assim.
**Data de nascimento é a exceção: continua exigindo dia, mês e ano completos**, porque é
ela que define a categoria do associado e o valor da cobrança — um dia inventado poderia
mudar o que a família paga. Data que não existe no calendário (31/02, por exemplo)
continua sendo recusada em qualquer coluna.

## Exemplo

O Grupo Trilha Verde tem uma planilha com 180 famílias, herdada de anos de controle
manual. Na primeira importação, a tesouraria escolhe **Ignorar existentes** — como é a
primeira vez, não há ninguém cadastrado ainda, então todo mundo entra. Três meses depois,
ao atualizar telefones e e-mails que mudaram, a tesouraria reimporta a mesma planilha
atualizada com a política **Preencher só campos vazios** — mantendo os dados que já foram
ajustados manualmente dentro do plugin.

## O que pode dar errado

- **"Nenhuma aba visível na planilha. Deixe visível a aba com os dados antes de enviar
  o arquivo."** — todas as abas do arquivo estão ocultas. Torne a aba de dados visível
  (no LibreOffice/Excel: botão direito na aba → **Reexibir**) e envie de novo.
- **A prévia mostra poucas linhas ou nomes que você não reconhece** — sinal de que a
  aba lida não é a de dados. Não processe: confira a ordem e a visibilidade das abas do
  arquivo, ou copie a aba de dados para um documento novo (veja a dica acima) e reenvie.
- **Algumas linhas deram erro** — a importação é parcial: as linhas sem erro são
  processadas normalmente. Volte à aba **Importação**, localize a importação na lista,
  clique em **Ver** e depois em **Baixar erros (CSV)** — o arquivo traz a linha, a
  mensagem do erro e os valores originais daquela linha, para corrigir na planilha e
  reimportar só o que faltou. Não precisa fazer isso na hora: o relatório continua
  disponível para consultar quando quiser, mesmo dias depois.
- **Coluna obrigatória sem mapear** — o sistema tenta adivinhar pelo nome da coluna na
  planilha, mas nem sempre acerta; confira o mapeamento antes de processar, especialmente
  se a planilha usa nomes de coluna fora do padrão.
- **Data inválida** (31/02, por exemplo) — a linha é recusada. Corrija a data na planilha
  e reimporte só o que faltou.
- **Arquivo maior que 5 MB ou 1000 linhas** — divida a planilha em partes menores e
  importe uma de cada vez.

## Depois de importar

A lista de importações (na mesma tela) mostra o **nome do arquivo como você enviou**, o
**status** de cada uma — **Concluída**, **Falhou** ou **Aguardando processamento** — e uma
coluna **Resultado**, por exemplo "269 entraram, 17 com erro". Importação ainda não
processada mostra "—" em Resultado.

{: .tip }
**O relatório de uma importação passada continua disponível — você não precisa corrigir
tudo na hora.** Importou 286 pessoas e viu 17 com erro? Pode voltar à lista mais tarde,
mesmo dias depois, clicar em **Ver**, baixar o CSV de erros, corrigir só essas linhas na
planilha original e reimportar apenas o que faltou — sem refazer a importação inteira.

Clique em **Ver** para abrir o relatório de uma importação já processada: contagens,
lista de erros linha a linha com o motivo, e o botão **Baixar erros (CSV)**.

![Relatório de uma importação: contagens, o erro linha a linha com o motivo, e o botão para baixar os erros em CSV](/assets/img/importacao-relatorio.png)

Numa importação enviada mas ainda não processada, **Ver** abre a pré-visualização de onde
você parou. Se o arquivo original não estiver mais no servidor, a tela avisa em vez de levar a
um link sem saída.

A lista também permite arquivar e desarquivar, inclusive em lote — útil para manter só as
importações recentes visíveis no dia a dia. Importações feitas antes desta mudança
mostram "Nome original não registrado" no lugar do nome do arquivo — é esperado, não é
erro.
