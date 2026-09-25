# Accessibility and performance audit

## Scope

Review the inbox, lead workspace, accessible widget lab, motion states, and both visual playgrounds. Check keyboard-only operation, visible focus, labels and names, error announcements, text contrast, 320 px reflow, reduced-motion behavior, and low-end mobile rendering. Use Lighthouse accessibility/performance and WAVE on the exact built version being reviewed.

## Current record

| Check | Status | Evidence |
|---|---|---|
| Semantic structure and keyboard paths | Component tests pass; manual keyboard and screen-reader review pending | Component tests and FE-03 notes |
| Automated WCAG A/AA scan | Passed with 0 reported violations on six primary routes | Playwright + axe-core; local Chromium run on 2026-09-25 |
| Reduced motion and static visual fallbacks | Implemented; browser preference check pending | Motion and 3D/shader source |
| Lighthouse mobile profile | Inbox 96 performance / 100 accessibility; lead review 97 / 98 | Saved HTML and JSON reports in `outputs/`; local production build, 2026-09-25 |
| WAVE violations | Not measured | WAVE extension report still required; no WAVE zero-error claim |
| Baseline versus after comparison | Not measured | Requires a stable preview URL |
| Mobile and browser matrix | Lighthouse mobile emulation measured; responsive widths and second browser not checked | Browser/device matrix remains in deployment checklist |

## Repeatable audit

1. Start the production build locally and open each route at 320 px, 768 px, and desktop width.
2. Lighthouse mobile reports are saved for the inbox and lead workspace. Repeat on a stable public preview before comparing revisions.
3. Run WAVE on the same URLs and record every error or contrast alert. Fix issues and rerun before claiming the capstone threshold.
4. Use keyboard only to traverse the nav, filter, open/close the dialog, change tabs, reveal disclosure content, submit a question, stop a response, and reach the static controls on reduced motion.
5. Compare performance with the visual playgrounds unloaded versus opened. Record actual values and device conditions; do not infer a score from implementation choices.

Both pages exceed the capstone's Lighthouse performance threshold of 85. The six-route axe scan reports no WCAG A/AA violations. WAVE, manual keyboard and screen-reader review, reduced-motion browser preference review, cross-browser checks, and a before/after comparison remain open; automated scans do not replace those checks.
