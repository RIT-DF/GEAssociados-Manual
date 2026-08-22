---
title: Importação de planilhas
nav_order: 5
---

# Importação de planilhas

Em **GE-Associados → Importação** você pode subir planilhas existentes (Excel/CSV) para criar
membros, responsáveis e famílias em lote, sem digitar tudo manualmente. O plugin reconhece
automaticamente os nomes das colunas mais comuns e agrupa membros pela mesma família quando o
CPF do responsável se repete.

## Quando usar

- **Primeira carga** — você acabou de instalar e tem uma planilha do Paxtu ou de outro sistema
  com seus membros atuais.
- **Atualização em massa** — recadastramento anual, mudança de seção, atualização de telefones.
- **Migração** — você tinha registros num Google Sheets ou planilha do financeiro e quer trazer
  tudo para o plugin.

## Modelo de planilha

Na tela de importação, clique em **Baixar modelo de planilha**. O arquivo já vem com os
cabeçalhos exatos que o sistema reconhece e três linhas de exemplo (dois irmãos com o mesmo
responsável, um voluntário e um membro estrangeiro sem CPF). Abra no Excel ou LibreOffice,
substitua os exemplos pelos seus dados e suba o arquivo de volta.

## Fluxo passo a passo

1. **Upload** — clique em *Enviar planilha*. O sistema valida o tamanho (até 5 MB) e o formato
   (.xlsx ou .csv).
2. **Preview** — você vê as primeiras 10 linhas para conferir se o arquivo subiu correto e os
   cabeçalhos estão na primeira linha.
3. **Mapeamento** — clique em *Continuar*. O sistema mostra cada coluna detectada com um menu
   para o campo de destino. Quando o cabeçalho é conhecido (ex.: "Nome", "CPF", "Ramo"), já vem
   pré-selecionado. Se uma coluna não foi reconhecida, escolha o destino manualmente ou marque
   *Ignorar*.
4. **Política de sobrescrita** — escolha como tratar registros que já existem (ver abaixo).
5. **Processar** — clique no botão e aguarde. O sistema processa até 1000 linhas em alguns
   segundos.
6. **Relatório** — você vê quantos foram criados, atualizados, ignorados e quantos deram erro.
   Linhas com erro mostram a mensagem e os valores originais para você corrigir. Há botão para
   baixar o relatório de erros em CSV.

## Cabeçalhos reconhecidos automaticamente

Você não precisa usar exatamente estes nomes — o sistema também reconhece variações (sem acento,
com letra maiúscula ou minúscula, com espaços extras). Mas quanto mais próximos do modelo, menos
ajuste manual no mapeamento:

| Campo | Cabeçalhos aceitos |
|---|---|
| Nome do membro | Nome, Nome do membro, Nome do jovem, Jovem, Membro, Associado |
| CPF do membro | CPF, CPF do membro, CPF do jovem |
| Data de nascimento | Data de nascimento, Data nascimento, Nascimento, DN, Aniversário |
| Data de ingresso | Data de ingresso, Data de associação, Data de admissão, Início da associação (opcional — usada no cálculo de pró-rata) |
| Tipo | Tipo, Categoria, Tipo de membro (valores: `jovem` ou `voluntário`) |
| Seção | Seção, Turma, Tropa, Patrulha |
| Ramo | Ramo |
| Número de registro | Registro, Matrícula, Paxtu |
| Sem CPF (estrangeiro) | Sem CPF, Estrangeiro (valores: `sim`, `yes`, `1`, `x`, `true`) |
| Nome do responsável | Responsável, Nome do responsável, Pagador |
| CPF do responsável | CPF do responsável, CPF responsável, CPF pagador |
| E-mail do responsável | E-mail, Email, E-mail do responsável, Email responsável |
| Telefone do responsável | Telefone, Celular, WhatsApp, Telefone do responsável |
| Nome do 2º responsável (opcional) | Responsável 2, Segundo responsável, Mãe, Pai |
| CPF do 2º responsável | CPF responsável 2, CPF mãe, CPF pai (sem máscara) |
| E-mail do 2º responsável | E-mail responsável 2, E-mail mãe, E-mail pai |
| Telefone do 2º responsável | Telefone responsável 2, Celular mãe, Celular pai |
| E-mail do membro | E-mail do membro, E-mail associado, E-mail do jovem (não dos responsáveis) |
| Data fim de cobrança | Data fim cobrança, Fim das cobranças, Data saída (a partir dessa data, o membro deixa de ser cobrado) |

## Agrupamento com Responsável 2

Quando a planilha trouxer um 2º responsável, o plugin faz o agrupamento de forma determinística:

- **Caso A — só R1:** comportamento padrão (membro vai para a família do R1).
- **Caso B-1 — só R2 informado, membro já existe:** anexa o R2 à família existente do membro.
- **Caso B-2 — só R2 informado, membro novo:** promove R2 a R1 (cria nova família com R2 como
  1º).
- **Caso C — R1 + R2:** cria/reusa ambos; se a família já tinha R2 diferente, substitui pelo
  informado na planilha.

## Política de sobrescrita

O sistema identifica membros existentes pelo CPF (e responsáveis também). Você escolhe o que
fazer quando um CPF já está cadastrado:

- **Ignorar** (padrão) — pula a linha. Útil para uma primeira importação onde você quer só
  completar lacunas, sem alterar quem já está no sistema.
- **Preencher apenas campos vazios** — atualiza só campos que estão em branco no cadastro
  existente. Útil para enriquecer dados sem sobrescrever ajustes manuais.
- **Sobrescrever todos os campos** — atualiza todos os campos com os valores da planilha. Útil
  em recadastramento anual completo.

Famílias nunca são "sobrescritas" — o sistema sempre tenta encontrar a família existente do
responsável (pelo CPF dele) e só cria uma nova quando não existir nenhuma.

{: .warning }
> A política de sobrescrita vale para a **linha inteira**. Se você escolher "Sobrescrever todos
> os campos" para corrigir um telefone desatualizado, um ajuste manual que alguém fez direto no
> cadastro (ex.: uma seção corrigida à mão) também é sobrescrito de volta ao valor da planilha,
> se a coluna estiver preenchida. Prefira "Preencher apenas campos vazios" quando não tiver
> certeza de que a planilha está mais atualizada que o cadastro.

## Membros estrangeiros sem CPF

Para membros que não têm CPF brasileiro (intercâmbio, jovens estrangeiros, etc.), deixe a coluna
**CPF** vazia e marque a coluna **Sem CPF** com `sim`. Sem essa marcação, o sistema rejeita a
linha — porque por padrão CPF é obrigatório para membros brasileiros e a ausência indica
esquecimento.

## Datas — formatos aceitos

O sistema aceita os formatos mais comuns de planilha brasileira:

- `dd/mm/aaaa` — `15/03/2014`
- `dd/mm/aa` — `15/03/14` (anos 00–69 viram 2000+, 70–99 viram 1900+)
- `dd-mm-aaaa` — `15-03-2014`
- `dd.mm.aaaa` — `15.03.2014`
- `aaaa-mm-dd` (ISO) — `2014-03-15`
- Células com tipo "Data" no Excel também funcionam.

## Erros comuns e como corrigir

| Mensagem | O que aconteceu | Como corrigir |
|---|---|---|
| Ramo 'X' não encontrado | O nome do ramo na planilha não bate com nenhum ramo cadastrado. | Verifique se o ramo existe em **Ramos**. O sistema é tolerante a acentos e caixa, mas o nome precisa ser parecido. Use "Lobinho" ou "Ramo Lobinho", por exemplo. |
| Seção 'X' não encontrada no ramo 'Y' | A seção existe no plugin, mas em outro ramo (ou não existe). | Confira em **Seções** a qual ramo a seção pertence. Cadastre se faltar. |
| Data 'X' não reconhecida | O formato da data não é nenhum dos aceitos. | Use um dos formatos listados acima. Se a célula é texto, verifique se não há caracteres extras. |
| CPF inválido | Os dígitos verificadores não batem. | Confirme o CPF no documento. Se for estrangeiro, deixe vazio e marque "Sem CPF" como `sim`. |
| CPF do membro é obrigatório | Linha de membro jovem com CPF vazio e sem marcar "Sem CPF". | Preencha o CPF ou marque a coluna "Sem CPF" como `sim` para estrangeiros. |
| Tipo 'X' não reconhecido | Valor na coluna Tipo não é `jovem` nem `voluntário`. | Use exatamente um desses dois valores (com ou sem acento). |
| Nome / E-mail do responsável é obrigatório | Linha de membro jovem sem nome ou e-mail do responsável. | Preencha os dois. Se for voluntário (adulto sem responsável separado), use Tipo = `voluntário`. |
| Planilha tem N linhas, acima do limite de 1000 | Arquivo grande demais para uma única importação. | Quebre em arquivos menores (ex.: por seção ou ramo) e suba um de cada vez. |

{: .note }
> Erros não interrompem o processamento — linhas boas são criadas/atualizadas mesmo se algumas
> falham. O relatório mostra exatamente quais linhas precisam de ajuste, com os valores
> originais. Corrija na planilha e re-suba só as linhas problemáticas (ou todas, se a política
> for "Ignorar").
