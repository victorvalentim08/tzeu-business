# TZEU Business — Development Guidelines

## Project

TZEU Business is a commercial management platform for TZEU Software House.

The initial goal is to create, manage, customize, publish and share professional commercial proposals through public URLs.

## Core principles

- Keep the codebase simple and maintainable.
- Prefer clear solutions over unnecessary abstractions.
- Do not add dependencies unless there is a clear reason.
- Do not change the project architecture without explicit approval.
- Do not rewrite working code unnecessarily.
- Follow existing project conventions before introducing new patterns.

## Technology

- Next.js
- TypeScript
- React
- Tailwind CSS
- shadcn/ui
- Base UI
- Lucide Icons
- Prisma
- PostgreSQL

## Next.js

- Use the App Router.
- Prefer Server Components by default.
- Use Client Components only when interactivity or browser APIs require them.
- Keep server-side and client-side responsibilities clearly separated.
- Use Server Actions or appropriate server-side mechanisms for mutations.

## TypeScript

- Use TypeScript throughout the application.
- Avoid `any`.
- Prefer explicit types for domain objects and function parameters.
- Keep types close to the domain they represent when appropriate.

## UI

- Use shadcn/ui components whenever an appropriate component already exists.
- Use Lucide for icons.
- Keep the interface professional, clean and consistent with a modern B2B SaaS.
- Avoid unnecessary visual complexity.
- Maintain responsive layouts.

## Database

- PostgreSQL is the database.
- Prisma is the ORM.
- Database access must remain on the server.
- Never expose database credentials to the client.
- Do not modify the database schema without considering migrations and existing data.

## Architecture

Prefer clear separation of responsibilities:

- UI components
- Domain logic
- Database access
- Validation
- Server-side actions
- Shared utilities

Do not create abstractions just for the sake of abstraction.

## Naming

- Components: PascalCase
- Functions and variables: camelCase
- Database models: PascalCase
- Database fields: camelCase
- Constants: camelCase unless a project convention requires otherwise
- Files should use the naming convention already established by the surrounding code.

## Dependencies

Before installing a new package:

1. Check whether the existing stack already solves the problem.
2. Check whether the dependency is actually necessary.
3. Prefer small, well-maintained dependencies.
4. Do not install libraries just because they are popular.

## Git

Use small, focused commits.

Commit messages should follow:

- `feat:` for new functionality
- `fix:` for bug fixes
- `refactor:` for code restructuring
- `chore:` for tooling/configuration
- `docs:` for documentation
- `test:` for tests

Example:

`feat: add proposal creation form`

## Agent behavior

Before implementing a significant feature:

1. Understand the existing architecture.
2. Inspect relevant files.
3. Explain the intended approach when the task is ambiguous.
4. Make the smallest reasonable change.
5. Do not modify unrelated files.
6. Do not install dependencies without explaining why.
7. Do not change database models without explicit approval.
8. Do not create mock implementations when real project functionality is expected.

When a requirement is unclear, ask for clarification instead of making large assumptions.