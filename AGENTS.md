# AGENTS.md

pi extension: task tools + live TUI widget. TypeScript, vitest. Runs from `src/index.ts` (package.json `pi.extensions`); `dist/` is a gitignored publish artifact, so no build step is needed to test local changes.

## Commands

| Command | What it does |
| --- | --- |
| `npx vitest run` | Full test suite. Run before handoff. |
| `npx tsc --noEmit` | Typecheck. Run with the tests. |

- When using a pi extension event: check it exists in this repo's `node_modules/@earendil-works/pi-coding-agent/dist/core/extensions/types.d.ts` — the pinned copy is the compile-time contract, while the installed pi decides what fires at runtime, and the two can drift.
