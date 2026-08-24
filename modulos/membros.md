---
title: Membros
parent: Módulos
nav_order: 6
---

# Membros

**Menu:** Associados → Membros

Cadastro dos jovens do grupo e dos adultos voluntários (chefia, escotistas).

![Lista de membros, com filtros por nome, ramo, seção, família e status](/assets/img/membros-lista.png)

## O que você faz aqui

Criar, editar, desativar e reativar membros — inclusive em lote. Filtre por nome, ramo,
seção, família e status; ordene por nome, tipo ou status.

## Campos do cadastro

![Formulário de novo membro](/assets/img/membro-formulario.png)

| Campo | Obrigatório | O que faz |
|---|---|---|
| Nome | Sim | |
| Tipo de membro | Sim | Pode afetar o cálculo de regras (ex.: regra específica para adulto voluntário) |
| CPF | Sim, salvo "Sem CPF (estrangeiro)" | Principal forma de o sistema reconhecer a mesma pessoa |
| Data de nascimento | Sim | Usada por regras que dependem de idade |
| Data de ingresso | Não | Em branco, usa a data do cadastro; afeta o cálculo de pró-rata |
| Data fim de cobrança | Não | Em branco, cobra indefinidamente |
| E-mail | Não | Menor de idade recebe as cobranças pelo e-mail do responsável, não pelo próprio |
| Família | Não | Pode ficar sem família — útil para um escotista adulto que não integra uma |
| Número de registro | Não | Precisa ser único na organização |
| Seção | Não | Preenche o campo Ramo automaticamente |
| Ramo | Não | |
| Foto | Não | |

## O que pode dar errado

{: .warning }
**Desativar um membro** interrompe a cobrança dele a partir dali, mas o histórico de
cobranças anteriores permanece — o sistema pede confirmação e explica isso na hora.
