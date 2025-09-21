# Repository Guidelines

## Project Structure & Module Organization
- `src/` – TypeScript + React app code. Entry: `src/main.tsx`; root component: `src/App.tsx`; styles: `src/*.css`; images/assets: `src/assets/`.
- `public/` – Static files served as-is (e.g., `favicon.svg`).
- `index.html` – Vite HTML entry.
- `vite.config.ts` – Build/dev configuration.
- `eslint.config.js`, `tsconfig*.json` – Linting and TypeScript config.
- Tests (when added) live next to source as `*.test.tsx` / `*.test.ts`.

## Build, Test, and Development Commands
- `yarn dev` – Start Vite dev server with HMR.
- `yarn build` – Type-check (`tsc -b`) and build production assets to `dist/`.
- `yarn preview` – Serve the production build locally for QA.
- `yarn lint` – Run ESLint across the project.

## Coding Style & Naming Conventions
- Language: TypeScript with React 19 function components.
- Indentation: 2 spaces; keep lines concise (~<100 chars when practical).
- Components: PascalCase file and symbol names (e.g., `Button.tsx`).
- Hooks: `useCamelCase`; colocate hook files with the feature using them.
- Assets: place under `src/assets/` and import via ESM.
- Linting: follow `eslint.config.js` (ESLint + typescript‑eslint + React Hooks rules). Fix warnings before committing.

## Testing Guidelines
- No runner configured yet. If adding tests, prefer Vitest + React Testing Library.
- Colocate tests with source as `*.test.tsx` / `*.test.ts`.
- Keep tests fast, deterministic, and UI‑focused at component boundaries.
- When introducing tests, add scripts (e.g., `"test": "vitest"`) and document usage in README.

## Commit & Pull Request Guidelines
- Commits: use Conventional Commits (`feat:`, `fix:`, `chore:`). Keep changes small and descriptive.
- PRs: include a summary, rationale, and scope. Link related issues. Add screenshots/GIFs for UI changes. Prefer small, focused PRs.

## Security & Configuration Tips
- Environment variables: use Vite `.env` files. Only `VITE_`-prefixed vars are exposed to the client. Do not commit secrets.
- Avoid storing credentials or tokens in code or `public/`.

## Agent-Specific Instructions
- This file governs the repository root. Obey its conventions for all edited files.
- Prefer minimal, localized changes; align with existing style; update docs when behavior or commands change.
- If nested `AGENTS.md` files exist, the deeper file takes precedence; direct user instructions override all.

