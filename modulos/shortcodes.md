---
title: Shortcodes
parent: Módulos
nav_order: 20
---

# Shortcodes

**Menu:** Configurações → aba Shortcodes

## Por que isto importa

O plugin publica conteúdo no site através de um **shortcode** — um código curto, entre
colchetes, que fica numa página do WordPress e vira o Portal do Responsável ou o
Simulador na hora em que o site é exibido. Na instalação, o plugin já cria essas páginas
para você; o shortcode é o que faz cada uma funcionar. Esta aba mostra os dois códigos,
prontos para copiar, para quem serve cada um, e o estado da página correspondente.

Ela também é o caminho de recuperação de quem apaga a página por engano: se a página
sumiu, o plugin avisa aqui e oferece recriar.

![Aba Shortcodes, com a tabela de atributos do gea_portal](/assets/img/configuracao-shortcodes.png)

## Os dois shortcodes

- **`[gea_portal]`** — o Portal do Responsável: pedir link de acesso, ver cobranças,
  baixar recibo e declaração. Para os responsáveis financeiros das famílias. Veja
  [Acompanhar e pagar as cobranças](/responsavel/portal/).
- **`[gea_simulador]`** — o Simulador público de valores: calcula quanto custaria
  participar, sem exigir cadastro. Para visitantes do site, sem necessidade de login.

Para cada um, a tela mostra:

- **Copiar código** — copia o shortcode para colar na página.
- O estado da página: **Página publicada**, com os botões **Ver página** e **Editar
  página**; ou um aviso de que a página não existe mais, com a opção de **criar uma
  nova**.
- **Ver no manual** — atalho para a página correspondente deste manual.

{: .tip }
**Apagou a página do portal ou do simulador sem querer?** Não precisa lembrar o
shortcode nem recriar a página do zero: abra esta aba, encontre o card do shortcode
sumido e use a opção de criar uma página nova. Ela nasce já com o shortcode certo
colado.

## Atributos do `[gea_portal]`

O `[gea_portal]` aceita seis atributos opcionais, para montar a página sob medida. **Sem
nenhum deles, a página fica exatamente como sempre foi** — os atributos só existem para
quem quer personalizar.

| Atributo | O que faz | Valores aceitos | Padrão |
|---|---|---|---|
| `titulo` | Mostra o título no topo da página. | `"sim"` ou `"nao"` | `"sim"` |
| `exibir` | Quais cobranças aparecem: todas, só as em aberto ou só as pagas. | `"tudo"`, `"aberto"` ou `"pago"` | `"tudo"` |
| `contato` | Mostra o card de troca do e-mail de contato. | `"sim"` ou `"nao"` | `"sim"` |
| `acessos` | Mostra o histórico de acessos ao portal. | `"sim"` ou `"nao"` | `"sim"` |
| `documentos` | Mostra a seção de documentos (recibo e declaração). | `"sim"` ou `"nao"` | `"sim"` |
| `limite` | Limita quantas cobranças aparecem na lista. | número inteiro maior que zero | sem limite |

{: .example }
Uma página que mostra só as cobranças em aberto, no máximo cinco:
`[gea_portal exibir="aberto" limite="5"]`

O `[gea_simulador]` não tem atributos — a página dele é sempre a mesma.

## Dicas e armadilhas

- **Valor inválido não quebra a página.** Se você digitar algo fora da lista aceita —
  por exemplo `exibir="pendente"`, que não existe — o shortcode ignora e usa o padrão
  em silêncio, em vez de mostrar erro. Errar a grafia de um atributo, então, não derruba
  a página; mas também não avisa que o atributo não fez efeito, então confira o
  resultado depois de colar.
- **`limite` corta a lista, mas avisa.** Quando há mais cobranças do que o limite
  permite mostrar, o portal exibe uma frase do tipo "E mais 3 itens." — o responsável
  sabe que existe mais coisa, mesmo sem ver tudo na tela.
- **Nenhuma combinação de atributos esconde o caminho para pagar.** Mesmo com
  `exibir="aberto"` e o restante desligado, uma cobrança em aberto sempre mostra o link
  de pagamento (quando ele existe) ou a orientação de a quem recorrer. Isso é
  proposital: os atributos controlam o que aparece **além** da lista de cobranças, nunca
  o acesso ao pagamento em si.

{: .warning }
Editar a página publicada pelo shortcode (o texto ao redor, por exemplo) é seguro — o
bloco do shortcode continua funcionando. Já **apagar o bloco do shortcode de dentro da
página** faz a página ficar em branco onde ele estava; se isso acontecer, volte aqui e
use **Copiar código** para colar de novo, ou recrie a página pela opção de recuperação.

## Quando dá errado

- **A aba avisa que a página foi apagada** — use o botão de criar uma página nova. Ela
  nasce publicada, com o shortcode já colado.
- **Colei o shortcode e não aconteceu nada** — confira se colou exatamente como está em
  **Copiar código**, sem espaço extra dentro dos colchetes, e se a página foi salva e
  publicada (não só como rascunho).
