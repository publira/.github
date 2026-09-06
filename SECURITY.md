# Security Policy

This policy applies to every repository in the [Publira](https://github.com/publira) organization that does not carry its own `SECURITY.md`. A repository that ships its own policy takes precedence over this one.

## Supported versions

Publira's repositories do not yet publish tagged releases, so security fixes are made on the `main` branch of the affected repository. Report a vulnerability against `main`, and expect the fix to land there. Once a repository starts tagging releases, its own `SECURITY.md` will say which of them are supported.

## Reporting a vulnerability

Report privately through the affected repository's **Security** tab, using **Report a vulnerability**. That opens the advisory form at `https://github.com/publira/<repository>/security/advisories/new`, which is visible only to you and the maintainers.

If private vulnerability reporting is not available on the affected repository, report through <https://github.com/publira/publira/security/advisories/new> instead and name the affected repository in the report.

Please do not report a vulnerability through a public Issue, pull request, or Discussion. A public report tells everyone about the problem before there is a fix to apply.

## What to include

The more of this a report carries, the sooner it can be reproduced and fixed:

- The affected repository, and the version or commit you tested.
- Steps to reproduce the problem, including any configuration or input needed.
- The impact as you understand it: what an attacker gains, and who is affected.

A proof of concept is welcome but not required. Send a report as soon as you are reasonably confident, rather than waiting until it is complete.

## What to expect

- Your report is acknowledged on the advisory thread as soon as we have read it, and that thread is where the rest of the conversation happens.
- We tell you whether we can reproduce the problem, and what we intend to do about it.
- The fix is coordinated with you: you are told when one is ready, and you are welcome to check that it addresses what you reported.
- Disclosure happens through a GitHub security advisory once a fix is available. You are credited as the reporter unless you ask us not to.

## Scope

This policy covers the source code of the repositories in the `publira` organization. It does not offer a bug bounty, and it does not authorize testing that degrades a service or touches data that is not yours.
