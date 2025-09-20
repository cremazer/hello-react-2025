# Repository Guidelines

## Project Structure & Module Organization
- `src/` – App source (TypeScript + React). Entry is `src/main.tsx`; root component is `src/App.tsx`; styles in `src/*.css`; images in `src/assets/`.
- `public/` – Static files served as-is (e.g., `favicon.svg`).
- `index.html` – Vite HTML entry.
- `vite.config.ts` – Build/dev config.
- `eslint.config.js`, `tsconfig*.json` – Linting and TypeScript configuration.

## Build, Test, and Development Commands
- `yarn dev` – Start Vite dev server with HMR.
- `yarn build` – Type-check (`tsc -b`) then build production assets to `dist/`.
- `yarn preview` – Serve the production build locally for QA.
- `yarn lint` – Run ESLint on the project.

## Coding Style & Naming Conventions
- Language: TypeScript with React 19 function components.
- Indentation: 2 spaces; keep lines concise (<100 chars when practical).
- Components: PascalCase file and symbol names (e.g., `Button.tsx`).
- Hooks: `useCamelCase` and colocate with the feature that uses them.
- Assets: place under `src/assets/`; import via ESM.
- Linting: follow `eslint.config.js` (ESLint + typescript‑eslint + React Hooks rules). Fix warnings before committing.

## Testing Guidelines
- No test runner is configured yet. If adding tests, prefer Vitest + React Testing Library.
- Place tests next to source as `*.test.tsx`/`*.test.ts`.
- Keep tests fast, deterministic, and UI-focused at component boundaries.

## Commit & Pull Request Guidelines
- Commits: follow Conventional Commits (e.g., `feat:`, `fix:`, `chore:`). Keep commits scoped and descriptive.
- PRs: include a summary, rationale, and scope. Link related issues. Add screenshots/GIFs for UI changes. Keep PRs small and focused.

## Security & Configuration Tips
- Environment variables: use Vite `.env` files; only variables prefixed with `VITE_` are exposed to the client. Do not commit secrets.
- Avoid storing credentials or tokens in code or `public/`.

## Working Notes for Automation/Agents
- Respect this file’s conventions when generating code.
- Keep changes minimal and localized; update docs when behavior or commands change.
