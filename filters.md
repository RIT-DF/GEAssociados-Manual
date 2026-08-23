---
title: Filtros e busca
parent: Cadastros
nav_order: 5
---

# Filtros e busca

A listagem de membros tem seis filtros que podem ser combinados livremente:

![Filtros na listagem de Membros](assets/img/members-list-filtered.png)
*Barra de filtros com Buscar, Ramo, Seção, Família, Status e Tipo.*

- **Buscar** — texto livre. Procura simultaneamente no nome do membro *e* no nome do responsável
  da família. Ex.: digitar "Souza" encontra membros vinculados à Família de Maria Souza, mesmo
  que o nome do membro não tenha "Souza".
- **Ramo** — dropdown com ramos ativos. Útil para listar "todos os Lobinhos".
- **Seção** — dropdown com seções ativas. Útil para listar "todos da Alcateia Lobos do Parque".
- **Família** — dropdown com famílias da organização. Útil para listar "todos os membros da
  Família X".
- **Status** — Ativos (padrão), Inativos ou Todos.
- **Tipo** — Jovens, Adultos voluntários ou Todos.

{: .tip }
> Os filtros são combináveis. Por exemplo: *Buscar "Pereira" + Ramo "Escoteiro" + Status
> "Ativos"* retorna apenas membros ativos do Ramo Escoteiro vinculados a uma família com
> responsável de sobrenome Pereira.

Clique em **Limpar** para voltar à listagem padrão (todos ativos, qualquer tipo).

## Filtros do Painel de cobranças

A tela **GE Associados → Cobranças** tem sua própria barra de filtros, focada no operacional
financeiro. São cinco filtros principais, todos combináveis:

- **Status** — Pendente, Pago, Cancelado, Aguardando pedido (WooCommerce) e *Vencido* (status
  derivado: pendente cujo vencimento já passou).
- **Plano** — dropdown com os planos ativos da organização. Útil para isolar "todas as
  mensalidades familiares semestrais".
- **Ciclo** — dropdown com os ciclos gerados. Pode vir pré-aplicado quando você clica no número
  da coluna "Cobranças" na tela de Ciclos.
- **Vencimento de / até** — intervalo de datas, útil para fechar relatórios mensais ("vencidas
  entre 01/01 e 31/01").
- **Buscar** — texto livre. Pesquisa simultaneamente no nome do membro, nome do responsável,
  número de matrícula e e-mail.

Veja também: [Painel de cobranças](charges).
