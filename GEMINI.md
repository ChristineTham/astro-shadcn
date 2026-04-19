# Project Context: Astro + React + shadcn/ui

This project is a modern web application built with **Astro**, **React**, and **Tailwind CSS v4**, integrated with **shadcn/ui** components.

## Project Overview
- **Framework:** Astro (v6+)
- **UI Library:** React (v19+)
- **Styling:** Tailwind CSS (v4) with `@tailwindcss/vite`
- **Component Library:** shadcn/ui (Base UI version)
- **Type Safety:** TypeScript
- **Fonts:** Noto Sans (sans-serif) and Noto Serif (heading) via Astro 6 native Fonts API (google provider).

## Core Architecture
- `src/pages/`: Contains the application routes (e.g., `index.astro`).
- `src/layouts/`: Base templates for pages (e.g., `main.astro`).
- `src/components/ui/`: Atomic UI components managed by shadcn/ui (using Base UI primitives).
- `src/lib/`: Utility functions and shared logic (e.g., `utils.ts` for Tailwind class merging).
- `src/styles/`: Global CSS and Tailwind v4 theme configurations.
- `astro.config.mjs`: Astro integration and Vite plugin configurations.
- `components.json`: shadcn/ui configuration for component generation.

## Key Commands
| Command | Action |
| :--- | :--- |
| `pnpm dev` | Starts the development server at `localhost:4321`. |
| `pnpm build` | Bundles the project for production. |
| `pnpm preview` | Previews the production build locally. |
| `pnpm typecheck` | Runs Astro and TypeScript type checks. |
| `pnpm lint` | Runs ESLint to check for code quality issues. |
| `pnpm format` | Formats all `.ts`, `.tsx`, and `.astro` files using Prettier. |
| `pnpm clean` | Removes build artifacts and `node_modules`. |
| `pnpm refresh` | Upgrades Astro and all dependencies to their latest versions. |
| `pnpm astro` | Run the Astro CLI directly. |

## Development Conventions
- **Path Aliases:** Use `@/` to reference the `src/` directory (e.g., `@/components/ui/button`).
- **Styling:** Tailwind CSS v4 is used. Custom theme variables (colors, spacing, etc.) are defined in `src/styles/global.css` using the `@theme` block.
- **Components:**
    - UI components MUST always be added via the `shadcn-cli` (e.g., `npx shadcn@latest add <component>`).
    - The project uses the `base-luma` style of shadcn components (Base-ui versions). Ensure any added components follow this pattern.
    - Do NOT manually copy-paste or create component files unless they are custom abstractions.
    - Prefer using the `Button` component from `@/components/ui/button` for consistency.
- **React in Astro:** Use the `client:load` or `client:visible` directives when adding interactive React components to Astro files.
- **Formatting:** Prettier is configured with plugins for Astro and Tailwind CSS class sorting. Run `pnpm format` before committing.
