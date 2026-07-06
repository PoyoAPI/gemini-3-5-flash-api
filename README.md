# Gemini 3.5 Flash API Examples for PoYo

[![Model page](https://img.shields.io/badge/Model%20page-gemini--3--5--flash-84cc16)](https://poyo.ai/models/gemini-3-5-flash)
[![API docs](https://img.shields.io/badge/API%20docs-docs.poyo.ai-22d3ee)](https://docs.poyo.ai/api-manual/chat-series/gemini-native-format)
[![License: MIT](https://img.shields.io/badge/License-MIT-111827)](LICENSE)
[![Main examples](https://img.shields.io/badge/Main%20examples-PoyoAPI%2Fpoyo--examples-0f172a?logo=github)](https://github.com/PoyoAPI/poyo-examples)

Focused server-side examples for building fast Gemini 3.5 Flash chat and assistant workflows on PoYo.

Gemini 3.5 Flash is useful for fast assistants, summarization, routing, product support flows, and agent steps where latency and throughput matter.

[Try on PoYo](https://poyo.ai/models/gemini-3-5-flash) | [Get API Key](https://poyo.ai/dashboard/api-key) | [Docs](https://docs.poyo.ai/api-manual/chat-series/gemini-native-format) | [Pricing](https://poyo.ai/pricing) | [Main Examples](https://github.com/PoyoAPI/poyo-examples)

## What This Repo Covers

- Chat completions with `gemini-3.5-flash`
- OpenAI-style `/v1/chat/completions` requests
- Server-side API key handling
- Node.js backend example
- Prompt examples and production integration notes

## Quick Start

```bash
cp .env.example .env
export POYO_API_KEY="your-api-key"
```

Run the Node.js example:

```bash
cd node
npm start
```

Keep `POYO_API_KEY` on the server. Do not expose it in browser code, mobile apps, screenshots, or public logs.

## Production Pattern

- Keep `POYO_API_KEY` on the server
- Send a chat completion request
- Log model, latency, and usage for cost tracking
- Add retries around network failures, not around every model response

## Models

This repo uses `gemini-3.5-flash`.

## Examples

| Path | What it covers |
| --- | --- |
| [`curl/generate.md`](curl/generate.md) | Copy-paste API request. |
| [`node/`](node/) | Native Node.js backend example. |
| [`docs/prompt-examples.md`](docs/prompt-examples.md) | Practical prompts for product workflows and creative tests. |
| [`docs/production-notes.md`](docs/production-notes.md) | Security and reliability notes before launch. |

## Run Checks

```bash
make check
```

On Windows:

```powershell
./scripts/check.ps1
```

## License

MIT
