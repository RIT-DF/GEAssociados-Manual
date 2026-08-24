---
title: Configurar um plano de cobrança
parent: Passo a passo
nav_order: 1
---

# Configurar um plano de cobrança

## Por que isto importa

O plano de cobrança é a base de tudo: ele diz quanto o grupo cobra, de quanto em quanto
tempo e de quem. Antes de existir um plano, não há como gerar cobrança nenhuma. Um plano
bem configurado desde o início evita ter que corrigir cobrança já emitida — coisa que o
plugin permite só até certo ponto (veja mais abaixo).

## Passo a passo

1. No menu, abra **Cobranças → Planos de cobrança**.
2. Clique em **Novo plano**.
3. Preencha:
   - **Nome** — o que aparece para quem vê a cobrança, por exemplo "Mensalidade 2026".
   - **Frequência** — mensal, trimestral, semestral, anual ou avulsa (cobrança única).
   - **Valor base** — o valor de tabela, antes de qualquer desconto ou acréscimo.
   - **Modo de cobrança** — individual (cada membro tem a sua), familiar (uma cobrança por
     família) ou híbrido.
   - **Modo de vencimento** — dia fixo do mês, relativo a um evento, ou definido em cada
     ciclo na hora de gerar.
   - **Categoria de produto do WooCommerce**, se o grupo cobra online.
4. Clique em **Salvar**.
5. Se o grupo pratica desconto, acréscimo, multa ou isenção, cadastre as regras
   correspondentes em **Cobranças → Regras** — veja
   [Módulos → Regras](/modulos/regras/) para o detalhe de cada tipo.

{: .tip }
Existe um **preset escoteiro** que cria de uma vez um plano e três regras já prontas
(desconto para irmãos, por exemplo). Ele não duplica o que já existir — se o grupo já tem
um plano parecido, o preset ignora e não cria de novo. Vale como ponto de partida para
quem está configurando o plugin pela primeira vez.

{: .warning }
**Renomeie o que o preset criar.** O plano e as três regras nascem com o sufixo
`(preset escoteiro)` no nome — marcador de origem, útil para você. Mas o nome da regra é
exibido no [simulador público](/responsavel/simulador/), onde quem ainda nem é associado
lê a explicação do valor. "Desconto Familiar (preset escoteiro)" numa página voltada a
pais soa como recado interno. Tire o sufixo depois de aplicar o preset.

## Exemplo

O Grupo Escoteiro Trilha Verde cobra uma mensalidade de R$ 80,00, mensal, por membro
(modo individual), com vencimento todo dia 10. Famílias com dois ou mais filhos no grupo
têm 20% de desconto a partir do segundo. O plano fica assim: nome "Mensalidade 2026",
frequência mensal, valor base R$ 80,00, modo individual, vencimento dia fixo (10). A regra
de desconto para o segundo filho é cadastrada à parte, em Regras.

## O que pode dar errado

- **Editar o valor de um plano não muda cobrança já gerada.** Só as cobranças de ciclos
  futuros usam o novo valor. Se você mudou o valor por engano e uma cobrança errada já
  saiu, corrija-a individualmente em
  [Detalhe da cobrança](/modulos/cobrancas/#detalhe-da-cobrança).
- **Plano com ciclo já gerado não pode ser excluído.** Se você criou um plano por engano e
  já gerou um ciclo nele, não dá para simplesmente apagar — resolva as cobranças daquele
  ciclo primeiro (cancelando, por exemplo).

## Próximo passo

Com o plano pronto, gere o primeiro ciclo em
[Acompanhar um plano de cobrança](/passo-a-passo/acompanhar-plano/).
