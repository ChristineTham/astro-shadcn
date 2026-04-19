# Astro + React + shadcn/ui + Base UI + Tailwind CSS

This is a modern web application template built with **Astro**, **React**, **shadcn/ui**, **Base UI**, and **Tailwind CSS v4**.

## Tech Stack

- **Framework:** [Astro](https://astro.build/) (v6+) for the core architecture and routing.
- **UI Library:** [React](https://react.dev/) (v19+) for interactive client-side components.
- **Components:** [shadcn/ui](https://ui.shadcn.com/) for a modular, accessible component architecture.
- **Primitives:** [Base UI](https://base-ui.com/) for unstyled, highly accessible UI primitives.
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/) for lightning-fast, utility-first styling.
- **Type Safety:** [TypeScript](https://www.typescriptlang.org/) for a robust development experience.

## Getting Started

### Adding Components

To add new shadcn/ui components to your project, you MUST always use the `shadcn-cli`. The project is configured to use the **Base UI** (formerly `base-luma`) style. Do NOT manually copy files into the `ui/` folder unless they are your own custom modifications.

```bash
npx shadcn@latest add <component-name>
```

Components will be automatically placed in the `src/components/ui/` directory.

### Using Components

To use the components in your application, import them within an `.astro` or `.tsx` file. Remember to use the `client:load` or `client:visible` directives when adding interactive React components to Astro files.

```astro
---
import { Button } from "@/components/ui/button"
---

<Button client:load>Get Started</Button>
```

## Available Scripts

| Command | Action |
| :--- | :--- |
| `pnpm dev` | Starts the development server at `localhost:4321`. |
| `pnpm build` | Bundles the project for production. |
| `pnpm preview` | Previews the production build locally. |
| `pnpm typecheck` | Runs Astro and TypeScript type checks. |
| `pnpm lint` | Runs ESLint to check for code quality issues. |
| `pnpm format` | Formats the codebase using Prettier. |
| `pnpm clean` | Removes build artifacts and `node_modules`. |
| `pnpm refresh` | Upgrades Astro and all dependencies to their latest versions. |
| `pnpm astro` | Run the Astro CLI directly. |
