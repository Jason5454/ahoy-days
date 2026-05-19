# AGENTS.md

## Cursor Cloud specific instructions

### Overview

This is a **shadcn-docs-nuxt** documentation starter site — a single Nuxt 3 application with no backend, database, or external service dependencies.

### Running the dev server

```bash
pnpm dev
```

Starts on `http://localhost:3000`. Hot-reload is enabled via Vite.

### Build

```bash
NUXT_IGNORE_LOCK=1 pnpm build
```

Use `NUXT_IGNORE_LOCK=1` if the dev server is already running, otherwise `pnpm build` will refuse to start due to Nuxt's dev-server lock.

### Gotchas

- **Ignored build scripts warning**: After `pnpm install`, you may see warnings about ignored build scripts for `@parcel/watcher`, `esbuild`, `sharp`, and `vue-demi`. Despite these warnings, the dev server and build both work correctly because pnpm bundles pre-built binaries for these packages.
- **`@nuxt/icon` disabled warning**: The `shadcn-docs-nuxt` theme pulls in `@nuxt/icon` which requires Nuxt 4+. This does not affect functionality in Nuxt 3 — icons still render via fallback mechanisms.
- **No lockfile committed**: The repo has no `pnpm-lock.yaml`. Running `pnpm install` will resolve the latest compatible versions each time.
- **No linter or test framework configured**: The project has no ESLint, Prettier, or test runner set up. Verification is done via `pnpm build`.
