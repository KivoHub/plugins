---
name: pesquisa-de-leis
description: Consulta o texto oficial de artigos de lei federal brasileira, súmulas do STF, STJ e TST e temas repetitivos e de repercussão geral, com o link da fonte. Use quando o pedido citar um artigo, uma súmula ou um tema, ou perguntar em qual lei está algo.
---

# Pesquisa de leis

Três ferramentas do servidor `kivohub-leis`. Escolha pela forma do pedido:

| O pedido | Ferramenta |
|---|---|
| Cita lei e artigo ("art. 11 da CLT", "CF art. 7º, XXIX") | `get_provision` |
| Cita súmula ou tema ("Súmula 331 do TST", "Tema 677 do STJ") | `get_precedent` |
| Descreve o assunto sem referência ("prazo para reclamar de vício aparente") | `search_legislation`, depois confirme com `get_provision` |

## Regras

- **Cite sempre o rótulo e o link oficial** que a ferramenta devolveu.
- **Nunca complete texto de memória.** Se a ferramenta não achou, diga que não achou nesta base.
- **Respeite o `status` de cada resultado:**
  - `verified`: texto conferido no Planalto, pode citar.
  - `unverified`: cite e avise que o texto ainda não foi conferido no site oficial.
  - `under_review`: o texto desta base difere do oficial. **Não cite o conteúdo**, mande consultar o link.
  - `revoked`: diga que o dispositivo foi revogado.
- **Precedentes:** informe o tribunal. O mesmo número de tema existe no STJ e no STF; se o pedido não disser qual, pergunte. Tema sem tese firmada não é direito, e tema sem repercussão geral não é tese vinculante: diga isso.
- **Pedido vago** ("precedentes", "lei do inquilinato"): pergunte o assunto ou o artigo antes de buscar.
- **Não dê parecer.** Cite a lei e indique procurar um advogado. A ferramenta é de pesquisa, não de orientação sobre caso concreto.

## Cobertura

Constituição, 14 leis e códigos federais (CC, CPC, CLT, CDC, CP, CPP, CTN, ECA, Lei 8.213, Maria da Penha, Inquilinato, LGPD, Juizados e Estatuto da Pessoa Idosa), súmulas do STF, STJ e TST, temas repetitivos do STJ e de repercussão geral do STF. Fora disso, a ferramenta não encontra.
