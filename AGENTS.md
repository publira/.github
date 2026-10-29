# .github Agent Guide

## What this repository is

This is the public `.github` repository of the Publira organization. GitHub reads four things from it:

- `profile/README.md`, the organization profile shown to visitors on <https://github.com/publira>. Signed-in members see the one in `publira/.github-private` instead.
- `SECURITY.md`, the default security policy for every Publira repository without one of its own.
- `pull_request_template.md`, the default pull request template for the same repositories.
- `renovate.json5`, the shared Renovate preset the other repositories extend with `github>publira/.github//renovate.json5`. A rule that applies to every Publira repository belongs here; a rule for one repository belongs in that repository's `.github/renovate.json5`.

The repository also publishes agent skills under `skills/`, installed in other repositories with `npx skills add https://github.com/publira/.github --skill <name>`. A skill's frontmatter holds only the Agent Skills standard fields (`name`, `description`), and its body names no organization, repository, or agent-specific substitution, so it works for every agent and for repositories outside Publira; anything specific to one repository belongs in that repository's `AGENTS.md`, which the skill reads.

The repository is public: nothing in it may carry credentials, tokens, or personal data.

## Language

Repository documentation, comments, commit messages, pull request text, and the profile are written in English.

Answer the user in the language of their own prose. Quoted logs, code, or UI strings do not decide it. Answer in English when no user prose settles it, such as in a scheduled or CI-started run.

## Git and pull requests

- Commit subjects and pull request titles use English Conventional Commits (`type(scope): description`).
- AI-assisted commits include an `Assisted-by: <agent>:<model id>` trailer, added with `git commit --trailer`. Never name an AI agent in a `Co-authored-by` trailer, in any capitalization.
- Keep each commit focused on one concern.
- Pull request descriptions follow `pull_request_template.md`: they explain the motivation, the main changes, and the verification performed, and end with the applicable `Assisted-by` trailer.

## Checks

- `pnpm check` runs the formatter and linter (oxfmt and oxlint through ultracite); `pnpm fix` applies the fixes. CI runs `pnpm check` on every pull request.
- `pnpm install` installs the lefthook pre-commit hook in `lefthook.yml`, which formats the staged JavaScript, TypeScript, CSS, JSON, Markdown, and YAML files with oxfmt and stages the result. It does not lint, so run `pnpm check` before committing. CI stays the source of truth; the hook can be bypassed with `--no-verify`.
- After changing `renovate.json5`, validate it with `pnpm --package=renovate dlx renovate-config-validator --strict renovate.json5`.
- Dependency updates come from Renovate. This repository's own `.github/renovate.json5` only extends the shared preset; change shared behavior in `renovate.json5` at the root.
