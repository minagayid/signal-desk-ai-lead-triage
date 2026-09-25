# Signal Desk

Signal Desk is an AI-assisted lead triage workspace for independent creative
studios. It helps a small team review project inquiries, see why a request may
fit, and prepare a useful follow-up. A person stays in control: the product
does not reject leads or send messages automatically.

The default qualification model is a small logistic-regression classifier
trained on synthetic examples. It returns evidence and a confidence estimate,
not a decision. The project is intentionally scoped as a portfolio application;
it is not a validated sales predictor and should not be used to make decisions
about people.

## Run locally

```powershell
cd web
npm install
npm run dev
```

Open `http://localhost:3000`. The local classifier needs no API key. Copy
`web/.env.example` to `web/.env.local` only if you later configure an optional
remote provider; never commit `.env.local`.

## Project map

- `web/src/app/` — app routes and server handlers
- `web/src/lib/ai/` — input validation, model, and qualification tool
- `web/src/components/` — lead workspace and reusable UI
- `docs/assignments/` — assignment-specific notes and evidence
- `docs/capstone/` — deployment checklist, audit, and reflection
- `SPEC.md` — audience, problem, scope, and AI role

## Quality checks

Run `npm run lint`, `npm run typecheck`, and `npm run test` from `web/` before
opening a pull request. The Playwright flow is documented in
`docs/assignments/TESTING.md` and uses local fixtures, never a live AI service.

## AI-assisted development

Codex helped map the assignment briefs, scaffold the project, and draft code.
The author reviewed generated changes and added or corrected validation,
keyboard behavior, evidence labels, and failure handling. See
[`docs/AI_WORKLOG.md`](docs/AI_WORKLOG.md) for the work log. Screenshots,
deployment and audit results are recorded only after they are actually captured.

## License

MIT. See [`LICENSE`](LICENSE).
