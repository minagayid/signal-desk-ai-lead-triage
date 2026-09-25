# Active task state

- **Goal:** prepare the 14 Frontend AI Engineering assignments and track-specific capstone as one reviewable project, with evidence grounded in work actually performed.
- **Non-goals:** submit portal work, publish a public repo/deployment, invent screenshots/research/audit results, or claim mentor approval.
- **Inputs:** authenticated Frontend AI Engineering “All” view and assignment briefs read 2026-09-25; user reliability contract; existing root repository and initial three Conventional Commits.
- **Local side effects:** code/docs, npm dependencies, local tests/audits, generated reports/screenshots, local commits/branches.
- **External boundary:** no remote configured. Public repo, hosted deployment, portal upload/submission, account changes, and secret entry remain pending a confirmed destination/action and final review.
- **Acceptance:** coherent app and practice routes, assignment evidence map, tests and production browser flow passing, Lighthouse scores recorded, 3+ Conventional Commits, genuine evidence only, clean secret review.
- **Recovery:** retain existing user files, keep outputs outside Git, make commits additive, return to `main` after branch comparison, review final status and history.

## Completed and verified

- Inspected the authenticated FE track: 14 assignments plus “Ship It—Your First Production AI Product.” Shared AI Fluency capstone is separate.
- Built Signal Desk with synthetic training data, local logistic-regression scoring, evidence/cautions, typed request validation, streamed explanation, interruption recovery, health route, and local failure demos.
- Added practice routes for React, keyboard-oriented widgets, cancellable button states, 3D scene, and GLSL shader; documented their implementation and limits.
- Added a 405-word workflow comparison and verified both local branches: vague prompt `5c89d0d`, precise prompt `605fb5f`; `main` contains the corrected version.
- Ran model training, lint, typecheck, 20 unit/component tests across 6 files, coverage, production build, and 10 Playwright checks across Chromium and Firefox. The six-route axe run found zero violations in both browsers; the dialog keyboard path, 320 px layout checks, and reduced-motion behavior also passed.
- Measured production Lighthouse mobile profile: inbox 96 performance/100 accessibility; lead detail 97/98. Full reports and screenshot are in ignored `outputs/`.

## Remaining

- Pending evidence: WAVE, manual screen-reader review, stable-URL baseline comparison, physical-device checks, genuine assistant-task screenshot, hosted CI.
- External completion remains: select public repo/host, deploy and smoke test, capture links, upload each artifact, submit, reopen portal to verify state, and obtain mentor review. No such action has been taken.
