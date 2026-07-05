# Gemini 3.5 Flash API cURL Quickstart

Use this from a backend environment. Keep `POYO_API_KEY` out of browser code.

```bash
export POYO_API_KEY="YOUR_POYO_API_KEY_HERE"

curl https://api.poyo.ai/v1/chat/completions \
  -H "Authorization: Bearer $POYO_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "model": "gemini-3.5-flash",
  "messages": [
    {
      "role": "system",
      "content": "You are a concise senior engineering assistant."
    },
    {
      "role": "user",
      "content": "Summarize the risks a developer should check before adding a fast model to a customer support assistant."
    }
  ],
  "max_tokens": 600
}'
```

## Notes

- Replace `YOUR_POYO_API_KEY_HERE` with a server-side environment variable in production.
- Start with `gemini-3.5-flash`, then route to other variants only when the workflow needs them.
- Log latency and usage so model routing decisions are based on real product behavior.

Model page: https://poyo.ai/models/gemini-3-5-flash
