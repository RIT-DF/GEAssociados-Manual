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

O caminho tem quatro paradas: enviar o arquivo, conferir a pré-visualização, mapear as
colunas e processar.

{: .important }
**Envie um arquivo com apenas a aba de dados.** O sistema lê a **primeira aba** da
planilha — inclusive se ela estiver oculta. Se você montou a aba de importação dentro da
planilha de trabalho do grupo, que costuma ter abas de controle antes dela, o que vai ser
lido é a primeira, e não a sua. O resultado não dá erro: aparece uma pré-visualização com
poucas linhas e nomes que você não reconhece.

{: .tip }
No LibreOffice ou no Excel, clique com o botão direito na aba de dados → **Mover ou copiar
planilha** → *Copiar* → destino **novo documento**. Você fica com um arquivo de uma aba só
para enviar, e a planilha de trabalho do grupo continua intacta.

![Tela de importação, passo de envio do arquivo](/assets/img/importacao.png)

Depois do envio, o sistema mostra as primeiras linhas do que leu. Vale conferir aqui: se
os dados aparecem trocados de coluna ou com acentuação estranha, o problema é do arquivo,
e é muito mais barato corrigir a planilha agora do que desfazer uma importação errada
depois.

![Pré-visualização das primeiras linhas lidas da planilha](/assets/img/importacao-previa.png)

Em seguida vem o mapeamento: para cada coluna da sua planilha, qual campo do sistema ela
alimenta. O sistema tenta adivinhar pelo cabeçalho; confira e ajuste. Use **Ignorar** nas
colunas que não devem ser importadas.

![Passo de mapeamento de colunas da importação](/assets/img/importacao-mapeamento.png)

## Referência rápida

- Formatos aceitos: **XLSX** ou **CSV**, até **5 MB** e **1000 linhas**.
- O sistema identifica quem já existe por **CPF** ou, na ausência dele, por **nome
  completo + data de nascimento**.
- A importação é **parcial**: linha com erro não desfaz o que já foi processado. Os erros
  saem em CSV para correção.
- A lista de importações permite ver, arquivar e desarquivar cada uma, inclusive em lote.
