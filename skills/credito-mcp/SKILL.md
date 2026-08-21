---
name: credito-mcp
description: Skill da REST API do Crédito & Score na MCP.AI: 11 endpoints em /api/credito. Score e análise de crédito de pessoas e empresas: score, dossiê, negativações, relatórios positivos, SCR do Banco Central e protestos. Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Crédito & Score — REST API skill

Você tem acesso à **Crédito & Score** REST API na MCP.AI.

> Score e análise de crédito de pessoas e empresas: score, dossiê, negativações, relatórios positivos, SCR do Banco Central e protestos. Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/credito
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/credito/detalhamento/negativo \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/credito/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (11)

#### `credito_detalhamento_negativo`

Detalhamento de negativações/pendências de um CPF ou CNPJ. _(POST /api/credito/detalhamento/negativo)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |

#### `credito_dossie`

Dossiê de crédito completo de um CPF ou CNPJ. _(POST /api/credito/dossie)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |

#### `credito_limite_pj`

Limite de crédito sugerido (positivo) de pessoa jurídica. _(POST /api/credito/limite/pj)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |

#### `credito_protestos`

Protestos em cartório (nacional) por CPF/CNPJ. _(POST /api/credito/protestos)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

#### `credito_protestos_sp`

Protestos em cartório de SP por CPF/CNPJ. _(POST /api/credito/protestos/sp)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

#### `credito_relatorio_pf_completo`

Relatório de crédito completo (positivo) de pessoa física. _(POST /api/credito/relatorio/pf/completo)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

#### `credito_relatorio_pf_mais`

Relatório de crédito (positivo, intermediário) de pessoa física. _(POST /api/credito/relatorio/pf/mais)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

#### `credito_risco_pj`

Risco de crédito (positivo) de pessoa jurídica. _(POST /api/credito/risco/pj)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |

#### `credito_score`

Score de crédito de um CPF ou CNPJ. _(POST /api/credito/score)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |

#### `credito_scr`

Resumo do SCR do Banco Central (histórico de crédito) — exige autorização do titular. _(POST /api/credito/scr)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

#### `credito_scr_detalhada`

SCR detalhado do Banco Central — exige autorização do titular. _(POST /api/credito/scr/detalhada)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `CNPJ` | string | Não | O parâmetro CNPJ pode ser enviado com ou sem formatação. |
| `CPF` | string | Não | O parâmetro CPF pode ser enviado com ou sem formatação. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_credito` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
