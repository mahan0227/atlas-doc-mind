# Atlas Doc Mind

Grounded document Q&A: answers must cite the text you provide, expose confidence, and suggest follow-ups when the document is thin. **Bring your own OpenAI API key** — keys stay in the browser except for proxied requests.

## Stack

Next.js 16 · React 19 · TypeScript · Tailwind CSS v4 · OpenAI Chat Completions (JSON mode)

## Run locally

```bash
npm install
npm run dev
```

1. Save your API key locally via the bar.
2. Paste a document and a question → **Ask with citations**.

## Notes

Very long documents consume tokens quickly; trim to the relevant sections for best results.

## License

MIT
