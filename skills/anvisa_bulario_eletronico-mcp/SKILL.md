---
name: anvisa_bulario_eletronico-mcp
description: Skill da REST API do ANVISA: Bulário Eletrônico na MCP.AI: 1 endpoint em /api/anvisa_bulario_eletronico. ANVISA: Bulário Eletrônico, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ANVISA: Bulário Eletrônico — REST API skill

Você tem acesso à **ANVISA: Bulário Eletrônico** REST API na MCP.AI.

> ANVISA: Bulário Eletrônico, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/anvisa_bulario_eletronico
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
curl -X POST https://api.mcp.ai/api/anvisa_bulario_eletronico/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/anvisa_bulario_eletronico/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `anvisa_bulario_eletronico_consultar`

ANVISA: Bulário Eletrônico, consulta em fonte oficial. _(POST /api/anvisa_bulario_eletronico/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `nome_medicamento` | string | Não | Parâmetro de consulta "nome_medicamento". |
| `numero_registro` | string | Não | Parâmetro de consulta "numero_registro". |
| `numero_expediente_bula_vigente` | string | Não | Parâmetro de consulta "numero_expediente_bula_vigente". |
| `empresa_cnpj` | string | Não | Parâmetro de consulta "empresa_cnpj". |
| `data_inicial` | string | Não | Parâmetro de consulta "data_inicial". |
| `data_final` | string | Não | Parâmetro de consulta "data_final". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_anvisa_bulario_eletronico` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
