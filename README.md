# Plugins da KivoHub

## pesquisa-de-leis

Texto oficial de artigos de lei federal brasileira, súmulas do STF, STJ e TST e temas repetitivos (STJ) e de
repercussão geral (STF), com o link da fonte. Gratuito, sem login. Servidor MCP: `https://leis.kivohub.ai/mcp`.

É uma ferramenta de pesquisa: não dá parecer nem orientação sobre casos. Os textos vêm do repositório
[ctresb/leis](https://github.com/ctresb/leis), conferidos com o Planalto; cada resultado informa se o texto foi
conferido, está em revisão ou foi revogado.

### Claude Code

```
/plugin marketplace add KivoHub/plugins
/plugin install pesquisa-de-leis@kivohub
```

Só o servidor, sem o plugin: `claude mcp add --transport http kivohub-leis "https://leis.kivohub.ai/mcp?src=claude-code"`

### Codex

```
codex plugin marketplace add KivoHub/plugins
codex plugin add pesquisa-de-leis@kivohub
```

Só o servidor, sem o plugin: `codex mcp add kivohub-leis --url "https://leis.kivohub.ai/mcp?src=codex"`

### ChatGPT, Claude.ai e outros clientes MCP

Adicione um conector personalizado com a URL `https://leis.kivohub.ai/mcp`, sem autenticação.

### Ferramentas

| Ferramenta | Para quê |
|---|---|
| `get_provision` | artigo, parágrafo, inciso ou alínea: `law="CLT", article="11"` |
| `get_precedent` | súmula ou tema: `court="TST", number="331"` |
| `search_legislation` | pergunta em linguagem natural, quando não há referência exata |

### Dados e limites

O servidor registra uma contagem de uso (ferramenta, lei consultada, resultado, tempo, cliente). Não guarda o texto
das perguntas nem o IP. Há limite de uso por IP e global. Detalhes em
[kivohub.ai/privacidade](https://kivohub.ai/privacidade#pesquisa-de-leis).

Licença MIT.
