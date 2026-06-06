# Repository Review Checklist

Use this checklist before writing about a GitHub repository, local project, archive, README, or set of project notes.

## Sources to Inspect

- `README`, `docs`, screenshots, demo links, and examples.
- Build and package files such as `package.json`, `requirements.txt`, `pyproject.toml`, `pom.xml`, `go.mod`, `Cargo.toml`, `Dockerfile`, and Compose files.
- Application entry points under folders such as `src`, `app`, `pages`, `routes`, `server`, `api`, `components`, and `lib`.
- Configuration examples such as `.env.example`, sample configuration, and deployment documentation.
- Tests, fixtures, seed data, and scripts when they reveal intended behavior.

## Facts to Extract

- Project name and purpose.
- Target user and problem addressed.
- Main user or system workflow.
- Tech stack and important libraries.
- Inputs, processing steps, outputs, and integrations.
- Installation, run, and demo instructions.
- Notable implementation details worth sharing.
- Limitations, TODOs, missing documentation, or unfinished areas.

## Accuracy Rules

- Treat project documentation and source files as primary evidence.
- Do not call a project production-ready unless the source supports that claim.
- Do not claim scale, users, revenue, benchmarks, security guarantees, or deployment status without evidence.
- Label code-supported but undocumented behavior as an inference.
- Ask for a repository archive, README text, or key files when the source cannot be accessed.
- Never quote secret values from credentials, tokens, private keys, or `.env` files.

## Brief Template

```markdown
Project:
Confirmed purpose:
Target user:
Tech stack:
Main flow:
Interesting implementation:
How to run:
Good LinkedIn angle:
Limitations or assumptions:
```
