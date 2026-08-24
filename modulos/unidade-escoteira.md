---
title: Unidade Escoteira
parent: Módulos
nav_order: 16
---

# Unidade Escoteira

**Menu:** Configurações → Unidade Escoteira

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
