---
name: ecrvsp_atpv_incluir-mcp
description: Skill da REST API do ECRVSP ATPV (Intenção de Venda): Incluir na MCP.AI: 1 endpoint em /api/ecrvsp_atpv_incluir. ECRVSP ATPV (Intenção de Venda): Incluir, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ECRVSP ATPV (Intenção de Venda): Incluir — REST API skill

Você tem acesso à **ECRVSP ATPV (Intenção de Venda): Incluir** REST API na MCP.AI.

> ECRVSP ATPV (Intenção de Venda): Incluir, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/ecrvsp_atpv_incluir
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
curl -X POST https://api.mcp.ai/api/ecrvsp_atpv_incluir/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"a3":"...","a3_pin":"...","login_cpf":"...","login_senha":"...","placa":"...","renavam":"...","chassi":"...","hodometro":"...","proprietario_email":"...","proprietario_cpf_cnpj":"...","comprador_cpf_cnpj":"...","comprador_nome":"...","comprador_email":"...","comprador_cep":"...","comprador_municipio":"...","comprador_bairro":"...","comprador_logradouro":"...","comprador_numero":"...","comprador_uf":"...","venda_valor":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/ecrvsp_atpv_incluir/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `ecrvsp_atpv_incluir_consultar`

ECRVSP ATPV (Intenção de Venda): Incluir, consulta em fonte oficial. _(POST /api/ecrvsp_atpv_incluir/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `a3` | string | Sim | Parâmetro de consulta "a3". |
| `a3_pin` | string | Sim | Parâmetro de consulta "a3_pin". |
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `placa` | string | Sim | Parâmetro de consulta "placa". |
| `renavam` | string | Sim | Parâmetro de consulta "renavam". |
| `chassi` | string | Sim | Parâmetro de consulta "chassi". |
| `hodometro` | string | Sim | Parâmetro de consulta "hodometro". |
| `proprietario_email` | string | Sim | Parâmetro de consulta "proprietario_email". |
| `proprietario_cpf_cnpj` | string | Sim | Parâmetro de consulta "proprietario_cpf_cnpj". |
| `comprador_cpf_cnpj` | string | Sim | Parâmetro de consulta "comprador_cpf_cnpj". |
| `comprador_nome` | string | Sim | Parâmetro de consulta "comprador_nome". |
| `comprador_email` | string | Sim | Parâmetro de consulta "comprador_email". |
| `comprador_cep` | string | Sim | Parâmetro de consulta "comprador_cep". |
| `comprador_municipio` | string | Sim | Parâmetro de consulta "comprador_municipio". |
| `comprador_bairro` | string | Sim | Parâmetro de consulta "comprador_bairro". |
| `comprador_logradouro` | string | Sim | Parâmetro de consulta "comprador_logradouro". |
| `comprador_numero` | string | Sim | Parâmetro de consulta "comprador_numero". |
| `comprador_complemento` | string | Não | Parâmetro de consulta "comprador_complemento". |
| `comprador_uf` | string | Sim | Parâmetro de consulta "comprador_uf". |
| `venda_valor` | string | Sim | Parâmetro de consulta "venda_valor". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_ecrvsp_atpv_incluir` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
