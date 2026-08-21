# Ferramentas

Crédito & Score expõe 11 ferramentas (todas somente leitura).

### 1. `credito_score`
**Input**: `CPF` (opcional), `CNPJ` (opcional), `completo` (opcional)

Score de crédito de um CPF ou CNPJ.

### 2. `credito_dossie`
**Input**: `CPF` (opcional), `CNPJ` (opcional), `completo` (opcional)

Dossiê de crédito completo de um CPF ou CNPJ.

### 3. `credito_detalhamento_negativo`
**Input**: `CPF` (opcional), `CNPJ` (opcional), `completo` (opcional)

Detalhamento de negativações/pendências de um CPF ou CNPJ.

### 4. `credito_relatorio_pf_completo`
**Input**: `CPF` (opcional), `completo` (opcional)

Relatório de crédito completo (positivo) de pessoa física.

### 5. `credito_relatorio_pf_mais`
**Input**: `CPF` (opcional), `completo` (opcional)

Relatório de crédito (positivo, intermediário) de pessoa física.

### 6. `credito_limite_pj`
**Input**: `CNPJ` (opcional), `completo` (opcional)

Limite de crédito sugerido (positivo) de pessoa jurídica.

### 7. `credito_risco_pj`
**Input**: `CNPJ` (opcional), `completo` (opcional)

Risco de crédito (positivo) de pessoa jurídica.

### 8. `credito_scr`
**Input**: `CNPJ` (opcional), `CPF` (opcional), `completo` (opcional)

Resumo do SCR do Banco Central (histórico de crédito) — exige autorização do titular.

### 9. `credito_scr_detalhada`
**Input**: `CNPJ` (opcional), `CPF` (opcional), `completo` (opcional)

SCR detalhado do Banco Central — exige autorização do titular.

### 10. `credito_protestos`
**Input**: `CNPJ` (opcional), `CPF` (opcional), `completo` (opcional)

Protestos em cartório (nacional) por CPF/CNPJ.

### 11. `credito_protestos_sp`
**Input**: `CNPJ` (opcional), `CPF` (opcional), `completo` (opcional)

Protestos em cartório de SP por CPF/CNPJ.

## Prompts de exemplo

```
Qual o score de crédito do CPF 000.000.000-00?
Esse CNPJ tem protestos ou negativações?
Mostre o dossiê de crédito completo dessa pessoa
```
