# Tasker
Tasker is a simple task management app built on top of a monorepo boilerplate using TypeScript, Go, and modern tooling.
## Features
- Create and manage tasks with a clean UI 
- Monorepo layout with separate `apps` and `packages` for better modularity.
- TypeScript for the frontend and shared libraries, Go for backend services.
- Turbo for task orchestration and fast incremental builds.
- Bun-based JavaScript tooling and Nixpacks config for easy deployment.
    
## Tech stack
- **Languages**: TypeScript, Go.
- **Monorepo tooling:** Turborepo (`turbo.json`).
- **JS runtime / package manager:** Bun (`bun.lock`).
- **Deployment:** Nixpacks (`nixpacks.toml`).

Your boilerplate section here, for example:

> This project is built on top of the `<your-boilerplate-name>` monorepo starter, which provides preconfigured tooling (linting, formatting, testing, and build pipelines).  
> Refer to the original boilerplate README for detailed conventions and scripts.

## Repository structure
```
├── apps/           # Application code (frontend, backend, etc.)
├── packages/       # Shared libraries and utilities
├── turbo.json      # Turborepo configuration
├── package.json    # Root package configuration
├── bun.lock        # Bun lockfile
├── nixpacks.toml   # Nixpacks deployment configuration
└── README.md
```


Inside `apps/` and `packages/`, describe what you actually have, e.g.:

- `apps/web`: Next.js/React frontend for Tasker.
- `apps/api`: Go or TS API server for task operations.
- `packages/ui`: Shared UI components.
- `packages/config`: Shared configuration and types.

## Getting started
---
## Prerequisites
- Node.js or Bun installed (depending on how your boilerplate runs scripts).
- Go (for backend services).
- (Optional) Docker if you plan to containerize.
    
Add your boilerplate’s typical setup here, for example:

## Development
Again, adapt this to match your boilerplate’s scripts:

```bash
# Run all apps in dev mode 
bun run dev 

# or, using turbo 
bun run turbo dev 

# Run only the web app 
bun run dev:web 

# Run only the API 
bun run dev:api
```


Link back to the boilerplate’s README for any shared commands:

> All standard development scripts (lint, test, build, etc.) are inherited from the base boilerplate.  
> See `../<boilerplate-README>` for the full list of commands and conventions.

## Environment variables
Document whatever your boilerplate requires plus any app-specific variables, for example:

```bash
API API_PORT=8080 DATABASE_URL=postgres://user:pass@localhost:5432/taskgo

# Web 
NEXT_PUBLIC_API_URL=http://localhost:8080
```

Add a note that these follow the same pattern as in the boilerplate.
## Building and deployment
Use your boilerplate’s build step plus Nixpacks:

```bash
#Build all apps 
bun run turbo build
```


If deploying with Nixpacks:
- Ensure `nixpacks.toml` is configured with the correct build and start commands.
- Point your platform (e.g., Railway, Fly.io) at this repository and let Nixpacks detect the stack.

Example:
```bash
# Start the production server(s) 
bun run start 
# or service-specific commands like 

bun run start:web 

bun run start:api
```
## Project conventions
- Code style, linting, and testing follow the base boilerplate’s configuration.
- Monorepo apps and packages should be small, focused, and share code via `packages/*`.
- Commit messages and branch naming follow the same conventions as the boilerplate; see the original README for details.
    