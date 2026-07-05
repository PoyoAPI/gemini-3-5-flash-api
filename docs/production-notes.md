# Gemini 3.5 Flash API Production Notes

## API Key Safety

- Keep `POYO_API_KEY` on the server.
- Do not place API keys in browser JavaScript, mobile apps, screenshots, analytics, or client logs.
- Store production keys in a secret manager or server environment variables.

## Request Handling

- Validate user input before sending it to PoYo.
- Log model, request type, status, latency, and task outcome.
- Retry network failures with backoff.
- Do not blindly retry model failures without reading the error reason.

## Cost Controls

- Start with the lowest-cost model path that can answer the product question.
- Promote to higher-quality variants only when the workflow needs it.
- Track usable outputs, failed tasks, retries, and manual cleanup time.

## Links

- Model page: https://poyo.ai/models/gemini-3-5-flash
- API docs: https://docs.poyo.ai/api-manual/chat-series/gemini-native-format
