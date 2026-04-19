# Volcengine Mem0 Memory Plugin

Hermes memory provider plugin for [Volcengine Mem0](https://www.volcengine.com/docs/86722) hosted service.

## Features

- Server-side LLM fact extraction and automatic deduplication
- Semantic search with optional reranking
- Circuit breaker protection for API failures
- Background prefetch and sync (non-blocking)
- Compatible with `hermes memory setup` configuration wizard

## Install

```bash
hermes plugins install imlida/hermes-volcengine-mem0
```

## Configuration

After installation, set the required environment variables in `~/.hermes/.env`:

```
VOLCENGINE_MEM0_API_KEY=your-api-key
VOLCENGINE_MEM0_HOST=https://your-host:8000
```

Optional variables:

```
VOLCENGINE_MEM0_USER_ID=hermes-user    # default
VOLCENGINE_MEM0_AGENT_ID=hermes        # default
```

Or configure via `hermes memory setup`.

## Activate

After installation, activate the memory provider:

```bash
hermes plugins
```

Navigate to **Provider Plugins > Memory Provider** and select **volcengine_mem0**.

## Tools

| Tool | Description |
|------|-------------|
| `volcmem0_search` | Search memories by semantic similarity |
| `volcmem0_conclude` | Store a durable fact about the user |
| `volcmem0_profile` | Retrieve all stored memories |

## Requirements

- Python package: `mem0ai`
- Volcengine Mem0 service credentials (API key + host)
