# Pior Labs

Pior Labs is a collection of self-hosted productivity tools built around a shared technical foundation for authentication, networking, deployment, data, and interface design.

## Backstory

What began as a finance-tracking application built to solve a personal problem gradually became something larger. As I started using AI-assisted development to move faster and take on more ambitious projects, I also began uncovering the gaps between building an application and operating a complete software platform. Each new requirement pushed me into a different area of software engineering.

- Wanting privacy led me into self-hosting.
- Wanting consistency led me to create a shared design-system package and reusable application foundation.
- Wanting simplicity led me to build a private authentication service.
- Wanting reliability pushed me toward containerized deployments, automated workflows, and centralized routing.
- Wanting maintainability led me to organize the work into dedicated application, service, package, and platform repositories.

AI accelerated the development process, but it also made ownership more important. Generated code still had to be understood, validated, integrated, secured, deployed, and maintained. Filling in those gaps became the real purpose of Pior Labs.

The result is no longer just a collection of applications built for a résumé. It is an evolving platform that demonstrates how I approach full-stack development, infrastructure, authentication, automation, system design, and the practical challenges of running software myself.

## Platform

The current platform foundation uses Docker Compose, a containerized Caddy edge, PostgreSQL, GitHub Actions, Tailscale, Cloudflare DNS, centralized OAuth/OIDC authentication, and a shared React design system.

Split-horizon DNS allows the same `*.szarans.ca` application URLs to resolve appropriately on the local network and over Tailscale, avoiding separate internal hostnames.

Finance is the first existing application to be fully migrated onto the shared platform model, including central SSO, platform networking, and PostgreSQL-backed persistence.

## Projects

| Repository | Purpose | Status |
| --- | --- | --- |
| [`app-dashboard`](https://github.com/pior-labs/app-dashboard) | Central launchpad for hosted applications | Active |
| [`service-auth`](https://github.com/pior-labs/service-auth) | Shared authentication and SSO | Active |
| [`package-design-system`](https://github.com/pior-labs/package-design-system) | Shared UI components and design tokens | Active |
| [`platform`](https://github.com/pior-labs/platform) | Public architecture and platform documentation | Active |
| [`app-finance-tracker`](https://github.com/pior-labs/app-finance-tracker) | Personal finance tracking | Active |
| [`template-webapp`](https://github.com/pior-labs/template-webapp) | Reusable starting point for new platform applications | Active |
| [`app-cookbook`](https://github.com/pior-labs/app-cookbook) | Recipe collection, cooking workflows, and meal planning | Active |
| [`service-health`](https://github.com/pior-labs/service-health) | Platform health and observability | Planned |
| `app-chatbot` | MCP-enabled platform assistant | Planned |

## Current direction

With the core platform foundation in place, current work is focused on building deeper application capabilities and using new projects to expand the platform deliberately:

1. Continue developing Cookbook beyond its core recipe experience, including meal planning, grocery-list generation, and broader MCP capabilities.
2. Build [`service-health`](https://github.com/pior-labs/service-health) as a small Go service to add practical Go experience while improving platform health and observability.
3. Keep refining the shared platform, deployment, and design-system conventions as new application requirements expose gaps.
4. Start the MCP-enabled AI chatbot once the supporting application capabilities and service patterns are mature enough to make the assistant genuinely useful.

## Status

Pior Labs is under active development. The core self-hosted platform foundation is operational; individual applications and platform capabilities will continue to evolve.

This is a personal portfolio organization. External pull requests are not currently accepted.
