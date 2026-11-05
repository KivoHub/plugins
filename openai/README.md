# Pacote para o diretório da OpenAI

Para enviar em https://platform.openai.com/plugins: gerar o zip com só estes três itens na raiz
(`plugin.json`, `mcp.json`, `assets/logo.svg`) e enviar em "Upload new or existing plugin".

```
cd openai/pesquisa-de-leis && zip -r ../pesquisa-de-leis.zip plugin.json mcp.json assets
```

O servidor é anônimo (sem OAuth), então não há credenciais nem conta de avaliação. Conferir os campos contra o
esquema aceito pelo portal no upload.
