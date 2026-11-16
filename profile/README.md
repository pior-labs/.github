# Pior Labs

Pior Labs is a collection of self-hosted productivity tools built on a shared foundation for authentication, networking, deployment, data, and interface design, and increasingly, a testbed for how AI agents can build and ship software responsibly.

## Backstory

What began as a finance-tracking application built to solve a personal problem gradually became something larger. As I started using AI-assisted development to move faster and take on more ambitious projects, I also began uncovering the gaps between building an application and operating a complete software platform. Each new requirement pushed me into a different area of software engineering.

- Wanting privacy led me into self-hosting.
- Wanting consistency led me to create a shared design-system package and reusable application foundation.
- Wanting simplicity led me to build a private authentication service.
- Wanting reliability pushed me toward containerized deployments, verified CI releases, and centralized routing.
- Wanting maintainability led me to organize the work into dedicated application, service, package, and platform repositories.
- Wanting agents to work across all of it led me to build a shared workspace of context, conventions, and decision records.

AI accelerated the development process, but it also made ownership more important. Generated code still had to be understood, validated, integrated, secured, deployed, and maintained. Filling in those gaps became the real purpose of Pior Labs, and the next step is making that discipline repeatable.

## Platform

The platform runs on Docker Compose, a containerized Caddy edge, PostgreSQL, GitHub Actions, Tailscale, Cloudflare DNS, centralized OAuth/OIDC authentication, and a shared React design system.

- **Split-horizon DNS** lets the same `*.szarans.ca` URLs resolve correctly on the local network and over Tailscale, with no separate internal hostnames.
- **Verified CI releases**: hosted CI validates and builds each release, and production deploys the exact image digests (or static archive checksums) from a successful main run instead of rebuilding on the host. Each repository keeps its own independent, manually triggered release, with readiness checks and current, previous, and failed release records for recovery.
- **Per-application isolation**: every app owns its database, schema, migrations, authorization, and CI, while the platform owns ingress, TLS, networking, and database provisioning.

## Agent workspace and software factory

Pior Labs is developed with AI agents, so the context they work from is treated as part of the platform.

- **Workspace**: a private multi-repository workspace that gives agents shared architecture docs, a service catalog, development conventions, architecture decision records, and one-command local setup, while every repository stays independent with its own history and CI.
- **New-app bootstrap**: a workspace skill that takes a new application from `template-webapp` through local development, application SSO, CI, and the related Auth and infrastructure changes across their owning repositories.
- **Software factory**: a staged agent workflow for application tasks: **plan** (scope and acceptance criteria approved by me), **build** (in an isolated worktree from a pinned base), **review** (by a fresh agent that never sees the builder's reasoning, against the approved requirements), bounded **repair** rounds, and **ship** (a pull request with CI monitored). Every stage leaves an auditable record. The skills are public in [`my-agent-context`](https://github.com/iPior/my-agent-context).

## Projects

| Repository | Purpose | Status |
| --- | --- | --- |
| [`app-cookbook`](https://github.com/pior-labs/app-cookbook) | Household recipes, scaling, meal planning, grocery lists, AI recipe import, and read-only MCP access | Active |
| [`app-finance-tracker`](https://github.com/pior-labs/app-finance-tracker) | Two-person finance tracking with conversational queries over MCP | Active |
| `app-tasks` | Deliberately simple task app used to prove out the software factory | Active (private) |
| [`app-chatbot-assistant`](https://github.com/pior-labs/app-chatbot-assistant) | MCP-enabled household assistant; SSO foundation live, chat in progress | Early |
| [`app-dashboard`](https://github.com/pior-labs/app-dashboard) | Central launchpad for hosted applications | Active |
| [`service-auth`](https://github.com/pior-labs/service-auth) | Shared authentication and SSO | Active |
| [`service-health`](https://github.com/pior-labs/service-health) | Go health aggregation service, built learning-first | In progress |
| [`package-design-system`](https://github.com/pior-labs/package-design-system) | Shared UI components and design tokens | Active |
| [`template-webapp`](https://github.com/pior-labs/template-webapp) | Starting point for new platform apps, with verified release tooling built in | Active |
| [`platform`](https://github.com/pior-labs/platform) | Public architecture, standards, and roadmap | Active |
| `platform-deploy` | Production routing, networking, and deployment automation | Active (private) |
| `workspace` | Multi-repo agent context, decision records, and setup tooling | Active (private) |

## Current direction

1. **Finalize the software factory using Tasks.** Tasks is intentionally small, so each feature exercises the factory rather than the product. The first full run, adding task creation, listing, and completion, went from approved plan through one repair round and an independent review pass to a merged PR. Each run feeds friction back into the workflow until it is something I can rely on for every app.
2. **Apply the factory to the rest of the platform**, starting with Cookbook and the Assistant once the workflow is stable.
3. **Build the Assistant's chat capabilities** on top of the MCP access Cookbook and Finance already expose.
4. **Continue `service-health`** as a hands-on Go project, with Dashboard as its first consumer.

## Status

Pior Labs is under active development. The self-hosted platform, verified release pipeline, and agent workspace are operational; applications and the software factory continue to evolve.

This is a personal portfolio organization. External pull requests are not currently accepted.
