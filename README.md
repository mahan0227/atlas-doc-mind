# Atlas Doc Mind

**Grounded document Q&A**: answers must cite spans from the text you provide, expose confidence, and suggest follow-ups when the document is too thin to support a strong answer.

## What it is

A BYOK Next.js app for **evidence-first** Q&A over a single pasted document (policy, RFC, contract excerpt, research PDF text, etc.). It refuses to hallucinate citations: if the doc doesn’t support an answer, the model says so.

## Why it’s useful

- Reduces **hallucinated “facts”** in internal knowledge workflows.
- Gives **confidence + follow-up questions** for analysts and reviewers.
- Short **verbatim citations** make answers checkable by humans.
- Faster than building a full RAG stack for one-off questions.

## Where you can use it

- **Legal / procurement** — first-pass Q&A on MSAs, DPAs, SOWs (not a substitute for counsel).
- **Engineering** — RFC and design-doc comprehension during onboarding.
- **Finance & ops** — memo and board-pack questions with traceability.
- **Support leads** — policy manual lookups when the CRM snippet is incomplete.

## Stack

Next.js 16 · React 19 · TypeScript · Tailwind CSS v4 · OpenAI Chat Completions (JSON mode)

## Run locally

```bash
npm install
npm run dev
```

1. Save your API key locally via the bar.
2. Paste a document and a question → **Ask with citations**.

## Production check

```bash
npm run build
npm run start
```

## API

`POST /api/ask` · Header `Authorization: Bearer <key>`

Body: `document` and `question` (required), optional `model`.

## Notes

Very long documents consume tokens quickly; trim to the relevant sections for best results.

## Suite brochure

[`docs/neuron-suite-brochure.html`](docs/neuron-suite-brochure.html) · [`docs/neuron-suite-ig-square.svg`](docs/neuron-suite-ig-square.svg)

## License

MIT
