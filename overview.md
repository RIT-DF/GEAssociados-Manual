---
title: Visão geral
nav_order: 2
---

# Visão geral

O **GE Associados** é um plugin WordPress que gerencia associados, famílias, responsáveis
financeiros e ciclos de cobrança. Foi pensado para grupos escoteiros, associações e outras
organizações associativas. A integração com WooCommerce permite cobrança online via gateway,
sem que você precise criar produtos públicos.

Desde a primeira versão, o plugin ganhou: **Wizard de onboarding** (configuração inicial em 9
passos), **Dashboard executivo** (KPIs e tendência de receita), **Comunicação por e-mail** (10
eventos configuráveis), **recálculo automático no checkout WooCommerce** (descontos por
pagamento antecipado, multas por atraso, isenções) e **auditoria detalhada** de cada cobrança.

![Menu lateral do GE Associados no wp-admin](assets/img/dashboard-menu.png)
*Menu lateral do plugin no wp-admin com todas as áreas disponíveis.*

## O que está pronto nesta versão

- Configuração da organização: nome, sigla, logo, cores, e-mail financeiro e fuso horário.
- Cadastro de **responsáveis financeiros**, **famílias** e **membros**, com validação de CPF
  brasileiro e suporte a membros estrangeiros.
- Estrutura de **Ramos e Seções**, com lista oficial da UEB já pré-cadastrada para grupos
  escoteiros.
- Listagem de membros com filtros por seção, ramo, família, tipo (jovem ou adulto voluntário),
  status e busca textual.
- **Importação** de planilhas Excel/CSV com mapeamento automático de colunas, agrupamento
  familiar por CPF do responsável e relatório de erros.
- **Motor de regras** com descontos, acréscimos, multas, isenções e créditos. Versionamento
  temporal das regras; simulador para testar antes de gerar cobranças.
- **Geração de ciclos de cobrança** com confirmação em 2 passos (preview do resumo antes de
  salvar). Modo individual e familiar; cobranças com snapshot imutável das regras vigentes.
- **Painel operacional de cobranças**: listagem cross-ciclo com filtros, tela de detalhe por
  cobrança com 5 tabs (Resumo, Cálculo, Snapshot, Membros, Histórico) e exportação XLSX.
- Cada plano de cobrança pode ter uma **categoria de produto WooCommerce**, para as cobranças
  aparecerem organizadas nos relatórios da loja. Ver [Planos de cobrança](billing-plans).
- Detecção automática de WooCommerce ausente e alerta visual quando necessário.

## O que vem por aí

- **Relatórios**: cobranças, membros e inadimplência em XLSX/CSV.
- **API REST**: integração com outros sistemas (sites próprios, planilhas, BI).
- **Módulo Eventos**: gestão de acampamentos, atividades e inscrições (em discussão).

Veja o tópico [Próximos passos](next-steps) para mais detalhes.
