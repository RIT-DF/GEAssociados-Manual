---
title: Importação
parent: Módulos
nav_order: 9
---

# Importação

**Menu:** Famílias e Membros → aba Importação

Traz membros, famílias e responsáveis de uma planilha, em vez de cadastrar um por um.
Veja o passo a passo completo em
[Importar dados de uma planilha](/passo-a-passo/importar-dados/).

O caminho tem até cinco paradas: enviar o arquivo, conferir a pré-visualização, mapear as
colunas, resolver ramo e seção (só aparece quando a planilha traz valor que ainda não
existe no sistema) e processar.

{: .important }
**Envie um arquivo com apenas a aba de dados.** O sistema lê a **primeira aba visível**
da planilha — abas ocultas são ignoradas. Se a sua planilha de trabalho tem, antes da aba
de dados, outra aba visível (uma capa, um resumo, um controle), é ela que vai ser lida, e
não a sua. O resultado não dá erro: aparece uma pré-visualização com poucas linhas e
nomes que você não reconhece — dado plausível, mas errado.

{: .tip }
No LibreOffice ou no Excel, clique com o botão direito na aba de dados → **Mover ou copiar
planilha** → *Copiar* → destino **novo documento**. Você fica com um arquivo de uma aba só
para enviar, e a planilha de trabalho do grupo continua intacta.

![Tela de importação, passo de envio do arquivo, com a orientação sobre a aba de dados](/assets/img/importacao.png)

Se o arquivo não tiver nenhuma aba visível, o envio é recusado com a mensagem "Nenhuma
aba visível na planilha. Deixe visível a aba com os dados antes de enviar o arquivo." —
torne a aba de dados visível e envie de novo.

Depois do envio, o sistema mostra as primeiras linhas do que leu. **É aqui que você
descobre se importou a planilha certa**: confira se o número de linhas bate com o
tamanho real da sua base e se os nomes das colunas são os que você espera. Planilha
errada lida não dá erro nenhum — só uma prévia enxuta e plausível, fácil de confundir com
"deu tudo certo". Se os dados aparecem trocados de coluna ou com acentuação estranha, o
problema é do arquivo, e é muito mais barato corrigir a planilha agora do que desfazer
uma importação errada depois.

![Pré-visualização das primeiras linhas lidas da planilha](/assets/img/importacao-previa.png)

Em seguida vem o mapeamento: para cada coluna da sua planilha, qual campo do sistema ela
alimenta. O sistema tenta adivinhar pelo cabeçalho; confira e ajuste. Use **Ignorar** nas
colunas que não devem ser importadas. Se a planilha tiver duas colunas com o mesmo nome
(duas "Observações", por exemplo), o mapeamento avisa a repetição e deixa mapear as duas
separadamente — nenhuma é descartada.

![Passo de mapeamento de colunas da importação](/assets/img/importacao-mapeamento.png)

Se a sua planilha usa nomes de ramo ou seção que ainda não existem no sistema, aparece um
passo próprio para resolver isso antes de processar: para cada valor novo, você escolhe
vincular a um ramo ou seção já cadastrado ou criar um. Ramo e seção **nunca** são criados
sozinhos pela importação — veja o passo a passo completo para o funcionamento detalhado.

## Referência rápida

- Formatos aceitos: **XLSX** ou **CSV**, até **5 MB** e **1000 linhas**.
- O sistema procura o cabeçalho nas primeiras linhas da planilha — não precisa ser a
  primeira — e avisa em qual linha o encontrou.
- Datas aceitam dia e mês com um dígito só e os separadores `/`, `-` e `.`. Data de
  ingresso e data fim de cobrança também aceitam só o ano ou mês e ano. Data de
  nascimento continua exigindo dia, mês e ano completos.
- O sistema identifica quem já existe por **CPF** ou, na ausência dele, por **nome
  completo + data de nascimento**.
- A importação é **parcial**: linha com erro não desfaz o que já foi processado. Os erros
  saem em CSV para correção.
- A lista de importações mostra o **status** de cada uma (Concluída, Falhou, Aguardando
  processamento) e permite ver, arquivar e desarquivar, inclusive em lote.
