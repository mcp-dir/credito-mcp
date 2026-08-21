# Crédito & Score

### Crédito & Score for Claude, ChatGPT and AI agents

Credit score and analysis for people and companies: score, dossier, defaults, positive reports, Central Bank SCR and protests. Platform-hosted, prepaid per query.

- 📊 **11 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Crédito & Score`, URL `https://api.mcp.ai/p_credito`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=credito&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jcmVkaXRvIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=credito&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_credito%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_credito
```

---

## 11 tools

| Tool | Description |
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

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_credito` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
