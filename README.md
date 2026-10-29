# Publira Community Health Files

Welcome to the `.github` repository for **Publira**.

This repository serves as a centralized hub for default community health files, templates, and configurations used across all open-source projects within the Publira organization.

By maintaining these files here, we ensure a consistent and welcoming experience for contributors, maintainers, and users across our entire ecosystem.

## What's in here?

- **[Organization Profile](profile/README.md):** The public landing page displayed at `https://github.com/publira`.
- **Issue & Pull Request Templates:** Default templates (`ISSUE_TEMPLATE`, `PULL_REQUEST_TEMPLATE.md`) to help contributors provide structured and actionable information when reporting bugs, requesting features, or submitting code.
- **Community Guidelines:** Centralized documents such as `CODE_OF_CONDUCT.md` and `CONTRIBUTING.md` to establish clear expectations and a safe environment for everyone.
- **[Security Policy](SECURITY.md):** How to report a vulnerability privately in any Publira repository, and what happens after a report arrives.

## Development

Open the repository in a [Dev Container](https://containers.dev/) (VS Code or GitHub Codespaces), or use Node.js and pnpm at the versions pinned in `package.json`.

```sh
pnpm install
pnpm check # format and lint
pnpm fix   # apply fixes
```

`pnpm install` also installs a [lefthook](https://github.com/evilmartians/lefthook) pre-commit hook that formats the staged JavaScript, TypeScript, CSS, JSON, Markdown, and YAML files with oxfmt. It does not lint them; `pnpm check` and CI do.

## Explore Our Ecosystem

To learn more about the tools we build for digital publishing, e-books, and webcomics, please visit our [Organization Profile](https://github.com/publira).

## License

[Apache License 2.0](LICENSE)
