# AGENTS.md

## Project overview


## Agent Docs
- `agent_docs/AGENTS.md`: repo rules and workflow expectations.
- `agent_docs/project.md`: fast orientation to the app, architecture, persistence model, and commands.
- `agent_docs/codex.md`: durable repo memory about breakages, root causes, and safe implementation patterns.
- `agent_docs/plans.md`: the standard for writing execution plans on large or risky tasks; it is not a history log.
- `agent_docs/task_master.md`: manager-agent guidance for triage, delegation, ownership boundaries, and integration across specialist agents.
- `agent_docs/docs-process.md`: durable playbook for docs, plans, and task-tracking specialists.
- `agent_docs/verification.md`: durable playbook for regression-test and verification specialists.
- `agent_docs/todo.md`: active and completed task tracking.

## Dev environment tips
- Use `npm install` to install dependencies.
- Use `npm run dev` for local development.
- Use `npm run build` to create the production bundle in `dist/`.
- Use `npm run preview` to verify the production build locally.
- Use `npm run lint` before finishing work. In this repo it runs TypeScript checks with `tsc --noEmit`.
- Use `npm run clean` to remove `dist/` when you need a clean build.
- Read `README.md` and `package.json` before adding new tooling so commands stay aligned with the project's current setup.

## Coding practices and conventions
- Prefer functional components and keep component responsibilities narrow.
- Reuse existing constants, utility helpers, and shared types before adding new patterns.
- Keep files focused. If a component starts handling unrelated concerns, split it into smaller units.
- Prefer ASCII in source files unless the file already requires other characters.
- Add comments so that a junior can understand and learn from the code.

## Testing and verification instructions
- Add or update tests if the repository later gains a test runner. For now, do not claim behavior is verified without at least running the available checks.

## Planning instructions
- For large, risky, or multi-step tasks, create and maintain an execution plan using `agent_docs/plans.md`.
- Use `agent_docs/plans.md` when the work spans multiple files, changes persisted data or PWA behavior, involves refactoring, or is likely to require handoff between agents.
- Follow the format and maintenance rules in `agent_docs/plans.md`, and keep the plan current as decisions, progress, and discoveries change.
- If you are acting as a manager agent and delegating work to other agents, read `agent_docs/task_master.md` before splitting the task.

## Change instructions
- Keep edits incremental and easy to review.
- Do not perform broad refactors unless they directly support the requested task.
- Call out tradeoffs when a feature request risks hurting bundle size, startup time, offline behavior, or phone usability.
- If you add a dependency, explain why it is necessary and why a lighter approach was not sufficient.
- Before finishing, confirm that commands and documentation still reflect the current repo state.
