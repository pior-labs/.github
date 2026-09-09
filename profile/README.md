# Pior Labs

Pior Labs is a self-hosted household productivity platform built around independently deployed applications that share authentication, networking, data infrastructure, UI conventions, and deployment workflows.

What began as a finance tracker has grown into a practical environment for building, deploying, and operating software at home. The platform now supports multiple real applications and is increasingly focused on making those applications work together rather than simply proving that the underlying infrastructure works.

## Why it exists

Pior Labs grew from solving personal problems while learning the parts of software engineering that sit beyond writing application code.

- **Privacy** led to self-hosting and private networking.
- **Consistency** led to a shared design system and reusable application template.
- **Identity** led to centralized OAuth/OIDC authentication.
- **Reliability** led to containerized deployments, CI/CD, health checks, routing, and operational tooling.
- **Maintainability** led to clear repository boundaries between applications, shared services, packages, public architecture, and private production configuration.
- **AI-assisted development** led to a stronger emphasis on documentation, repeatable patterns, validation, and understanding the systems being generated and operated.

The result is an evolving personal platform for exploring full-stack development, infrastructure, authentication, automation, system design, and AI-enabled application integration through software that is actually used.

## Applications

| Application | Repository | Purpose | Status |
| --- | --- | --- | --- |
| Dashboard | [`app-dashboard`](https://github.com/pior-labs/app-dashboard) | Home entry point for Pior Labs applications | Active |
| Finance | [`app-finance-tracker`](https://github.com/pior-labs/app-finance-tracker) | Private household finance tracking and analysis | Active |
| Cookbook | [`app-cookbook`](https://github.com/pior-labs/app-cookbook) | Shared recipes, cooking workflows, and meal-planning capabilities | Active |

Cookbook is the first application built end-to-end from the standardized Pior Labs application template after the shared platform model was established. Its initial recipe-management experience is operational, and its MCP interface demonstrates how application capabilities can be exposed to trusted AI clients without creating a second data layer.

## Shared platform

The current platform foundation includes:

- Docker Compose for self-hosted application deployment
- Caddy for centralized routing and TLS
- PostgreSQL with application-specific databases and roles
- centralized OAuth/OIDC authentication through [`service-auth`](https://github.com/pior-labs/service-auth)
- a shared React design system through [`package-design-system`](https://github.com/pior-labs/package-design-system)
- Tailscale for private remote access
- Cloudflare DNS and split-horizon DNS for stable `*.szarans.ca` application hostnames
- GitHub Actions with repository-scoped self-hosted runners
- reusable application conventions through [`template-webapp`](https://github.com/pior-labs/template-webapp)

Public architecture and platform conventions live in [`platform`](https://github.com/pior-labs/platform). Production deployment configuration remains separate in the private `platform-deploy` repository.

## Application-owned MCP

Pior Labs is moving toward application-owned MCP interfaces for trusted AI workflows.

Rather than giving an assistant direct database access or building one central integration layer that reimplements application logic, each application can expose narrow capabilities backed by its existing domain rules.

Cookbook is the first working example. This creates a path toward conversational workflows such as finding and scaling recipes, building meal plans, generating grocery lists, and eventually coordinating useful actions across multiple Pior Labs applications.

## Repository model

| Repository pattern | Responsibility |
| --- | --- |
| `app-*` | User-facing applications |
| `service-*` | Independently deployed shared services |
| `package-*` | Shared libraries and design-system packages |
| [`platform`](https://github.com/pior-labs/platform) | Public architecture, conventions, and roadmap |
| `platform-deploy` | Private production infrastructure and operations |
| [`template-webapp`](https://github.com/pior-labs/template-webapp) | Reusable starting point for new applications |
| `.github` | Organization profile and shared GitHub configuration |

## Current direction

The platform has moved beyond its initial **foundation-building** stage. The shared authentication, routing, database, design-system, application-template, and deployment patterns are operational and have been exercised by multiple applications.

Current work is focused on:

1. **Deepening existing applications** — beginning with Cookbook meal planning and grocery-list generation rather than continuously creating new standalone apps.
2. **Expanding application-owned MCP capabilities** as useful conversational workflows emerge.
3. **Building toward cross-application assistance** where a future Pior Labs assistant can compose capabilities exposed by individual applications.
4. **Keeping the paved road reusable** so future applications inherit the same auth, networking, UI, database, and deployment conventions.
5. **Hardening operations** through better observability, deployment verification, backup, and restore procedures.

The long-term goal is a coherent household productivity system made of independently owned applications that can also work together through stable platform conventions and narrow AI-facing interfaces.

## Learn more

For architecture, repository boundaries, deployment patterns, networking, security, and the current roadmap, see the [`pior-labs/platform`](https://github.com/pior-labs/platform) repository.

Pior Labs is under active development and is primarily a personal engineering and portfolio project. External pull requests are not currently accepted.
