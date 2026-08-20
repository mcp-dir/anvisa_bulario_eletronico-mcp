# Instalação detalhada

ANVISA: Bulário Eletrônico é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_anvisa_bulario_eletronico`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_anvisa_bulario_eletronico` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_anvisa_bulario_eletronico` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_anvisa_bulario_eletronico` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.anvisa_bulario_eletronico` (ou `servers.anvisa_bulario_eletronico` no VS Code) do config do cliente e reinicie.
