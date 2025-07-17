# Repository Agent Guidelines

The information below explains how Codex agents should work with this repository.

## Environment
- **Node.js**: The project requires Node.js 22.15.0. Use a version manager (`nvm` or similar) to match the version in `.nvmrc`/`.node-version`.
- **Yarn workspaces**: Every directory under `packages/` is a separate workspace. Run `yarn install` inside the package you are modifying to install or update dependencies.

## Pre-commit checklist
1. Run `yarn lint` to check ESLint and Prettier rules. The Prettier config (`.prettierrc.js`) enforces single quotes. You can run `yarn lint --fix` to format automatically.
2. Run `yarn test` in packages that contain tests.

## Commit conventions
- Follow the [Conventional Commits](https://www.conventionalcommits.org) standard. Examples: `feat(web): add dark mode`, `fix(backend): handle null user id`.
- Keep commit messages short but descriptive and group related changes together.

## Documentation
- Update docs under `packages/docs` or the root `README.md` whenever features or behaviour change.
