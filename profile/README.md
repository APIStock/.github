# API Stock

**One API key and one prepaid balance for AI video, image, music and chat models.**

[API Stock](https://api-stock.com) puts Veo, Kling, Seedance, Wan, Nano Banana,
GPT Image, Seedream, Suno, Claude, GPT, Gemini, DeepSeek and other models behind
one REST API. Media requests are priced up front, queued, and retried on a
reserve provider if the first one fails. Results are stored on our side and
delivered by polling or webhook.

- **Models and prices:** <https://api-stock.com/models>
- **Docs and API reference:** <https://docs.api-stock.com>
- **Chat:** OpenAI-compatible `POST /api/v1/chat/completions` and
  Anthropic-compatible `POST /api/v1/messages`
- **Media:** `POST /api/v1/generation/create`, then `GET /api/v1/task/status/{taskId}`
- **Top-ups:** cards, Alipay, WeChat Pay and crypto

```sh
curl https://api.api-stock.com/api/v1/generation/create \
  -H "Authorization: Bearer $API_STOCK_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"nano-banana-pro","input":{"prompt":"A quiet lighthouse at blue hour"}}'
```

## Repositories

| Repository | What it is |
| --- | --- |
| [api-stock-examples](https://github.com/APIStock/api-stock-examples) | Starter code in TypeScript, Python and curl: chat, media tasks, webhooks, a Telegram bot |
| [api-stock-mcp](https://github.com/APIStock/api-stock-mcp) | Hosted MCP server for Claude Code, Codex, Cursor and other MCP clients (`https://api.api-stock.com/mcp`, OAuth sign-in) |
| [api-stock-openclaw](https://github.com/APIStock/api-stock-openclaw) | OpenClaw skill for image, video and music generation |

Questions: [support@api-stock.com](mailto:support@api-stock.com)
