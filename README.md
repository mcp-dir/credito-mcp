# Crédito & Score

### Crédito & Score para Claude, ChatGPT e agentes de IA

Score e análise de crédito de pessoas e empresas: score, dossiê, negativações, relatórios positivos, SCR do Banco Central e protestos. Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago.

- 📊 **11 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Crédito & Score` e **URL** `https://api.mcp.ai/p_credito`.

### Cursor

[➕ Instalar Crédito & Score no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=credito&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jcmVkaXRvIn0=)

### VS Code (Copilot Chat)

[➕ Instalar Crédito & Score no VS Code](vscode:mcp/install?name=credito&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_credito%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_credito
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Qual o score de crédito do CPF 000.000.000-00?
Esse CNPJ tem protestos ou negativações?
Mostre o dossiê de crédito completo dessa pessoa
```

---

## 11 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `credito_score` | Score de crédito de um CPF ou CNPJ. |
| `credito_dossie` | Dossiê de crédito completo de um CPF ou CNPJ. |
| `credito_detalhamento_negativo` | Detalhamento de negativações/pendências de um CPF ou CNPJ. |
| `credito_relatorio_pf_completo` | Relatório de crédito completo (positivo) de pessoa física. |
| `credito_relatorio_pf_mais` | Relatório de crédito (positivo, intermediário) de pessoa física. |
| `credito_limite_pj` | Limite de crédito sugerido (positivo) de pessoa jurídica. |
| `credito_risco_pj` | Risco de crédito (positivo) de pessoa jurídica. |
| `credito_scr` | Resumo do SCR do Banco Central (histórico de crédito) — exige autorização do titular. |
| `credito_scr_detalhada` | SCR detalhado do Banco Central — exige autorização do titular. |
| `credito_protestos` | Protestos em cartório (nacional) por CPF/CNPJ. |
| `credito_protestos_sp` | Protestos em cartório de SP por CPF/CNPJ. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Pré-pago (carteira de créditos), paga por uso. Veja [docs/precos.md](docs/precos.md).

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_credito`.


---

## Suporte

- 📧 [credito@mcp.ai](mailto:credito@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/credito-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_credito` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
