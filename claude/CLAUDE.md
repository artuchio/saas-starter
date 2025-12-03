# Development Workflow

## Pre-Implementation
1. Explore the codebase to understand relevant files and existing patterns
2. Use the TodoWrite tool to create a task breakdown
3. Present the plan and wait for approval before proceeding

## Implementation
1. Work through tasks systematically, marking each complete as you finish
2. Provide high-level summaries of changes at each step (not verbose explanations)
3. When bugs occur, identify and fix root causesno temporary workarounds

## Code Quality Principles
- **Simplicity First**: Minimize scope of changes. Modify only what's necessary for the task
- **No Over-Engineering**: Don't add features, refactoring, or "improvements" beyond what's requested
- **Focused Changes**: Each change should impact the smallest possible surface area
- **Zero Assumptions**: If requirements are ambiguous, ask before implementing

## Post-Implementation
After completing all tasks, add a brief summary to the [Copilot Journal](./JOURNAL.md) including:
- What was changed and why
- Any architectural decisions made
- Relevant context for future work

See [JOURNAL.md](./JOURNAL.md) for structured entry format and examples.

## Project Context
This is a Next.js 15 SaaS starter using:
- **Frontend**: React 19 with TypeScript (strict mode)
- **Database**: PostgreSQL with Drizzle ORM
- **Auth**: JWT-based with server actions
- **Payments**: Stripe integration
- **UI**: Tailwind CSS + shadcn/ui components
- **Package Manager**: pnpm

### Common Patterns
- Server components by default, use Server Actions for mutations
- Use `validatedAction` middleware for form handling
- Keep database queries in `lib/db/queries.ts`
- Add activity logs for important user actions
- Follow path alias imports (`@/*`)
