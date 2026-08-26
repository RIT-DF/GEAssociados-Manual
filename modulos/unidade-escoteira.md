---
title: Unidade Escoteira
parent: Módulos
nav_order: 16
---

# Unidade Escoteira

**Menu:** Configurações → aba Unidade Escoteira

Os dados do grupo: identificação, contato, endereço, fuso horário e identidade visual.

![Tela de configuração da unidade escoteira preenchida](/assets/img/unidade-escoteira.png)

## Campos

| Campo | Obrigatório | O que faz |
|---|---|---|
| Nome | Sim | |
| Sigla | Não | Até 20 caracteres |
| CNPJ | Não | Opcional porque nem todo grupo tem |
| Contato e endereço | Não | O CEP busca o resto do endereço sozinho ao sair do campo |
| Fuso horário | Sim | Decide quando as cobranças saem e como as datas aparecem em todo o plugin |
| Identidade visual (logo, cor primária e secundária) | Não | Em branco, herda o tema do site |

{: .important }
O **fuso horário** não é um detalhe cosmético: ele decide a que hora local os e-mails
automáticos disparam e como as datas de vencimento são interpretadas. Configure-o
corretamente antes de gerar o primeiro ciclo de cobrança.

## Tamanho da logo, para sair nítida no recibo e na declaração

O recibo e a declaração anual (veja
[Baixar recibo](/modulos/cobrancas/#baixar-recibo-tesouraria) e
[Declaração anual](/modulos/familias/#declaração-anual)) desenham a logo cadastrada aqui
numa altura que respeita a resolução do arquivo — em vez de esticar sempre para o mesmo
tamanho.

{: .tip }
Para a logo sair no **tamanho cheio** nesses documentos, o arquivo precisa ter pelo menos
**~190 px de altura**. Abaixo disso, o sistema reduz o desenho para manter a nitidez na
impressão: a logo sai menor, mas nítida, em vez de grande e serrilhada. Para o melhor
resultado impresso, prefira um arquivo com largura de **1000 px ou mais**.

{: .note }
Se o arquivo não puder ser lido — corrompido, ou num formato diferente de JPEG/PNG —, o
documento continua sendo gerado, só que sem a logo, e o [Diagnóstico](/modulos/diagnostico/)
mostra um aviso até você recadastrar o arquivo.
