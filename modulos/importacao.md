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
