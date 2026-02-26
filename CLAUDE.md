# wopr-plugin-browser

Browser automation plugin for WOPR using Playwright.

## Build & Test

```bash
npm install
npm run build      # tsc
npm run check      # biome check + tsc --noEmit
npm run test       # vitest run
npm run lint       # biome check
npm run lint:fix   # biome check --fix
npm run format     # biome format --write
```

## Architecture

- `src/index.ts` — Plugin entry point, default export, A2A tool registration
- `src/browser.ts` — Playwright browser management, A2A tool handlers, SSRF protection
- `src/browser-profile.ts` — Profile persistence via WOPR Storage API
- `src/browser-profile-schema.ts` — Zod schemas + PluginSchema for storage tables

## Plugin Contract

- Imports types from `@wopr-network/plugin-types` only — no relative imports into core
- Uses `PluginSchema` + `Repository` for storage (never raw Drizzle)
- A2A tools registered via `ctx.registerA2AServer()` (guarded)
- `shutdown()` closes all browsers, resets storage reference, idempotent

## Issue Tracking

Tracked in Linear under the WOPR team.
