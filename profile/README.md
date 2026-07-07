# Pior Labs

Pior Labs is a collection of self-hosted productivity tools that needed structure, coherence, and a shared technical foundation to grow into a reliable, maintainable platform.

## Backstory

What began as a finance-tracking application built to solve a personal problem gradually became something larger. As I started using AI-assisted development to move faster and take on more ambitious projects, I also began uncovering the gaps between building an application and operating a complete software platform. Each new requirement pushed me into a different area of software engineering.

- Wanting privacy led me into self-hosting.
- Wanting consistency led me to create a shared design-system package. I created a reusable foundation that future web applications could depend on from the beginning.
- Wanting simplicity led me to build a private authentication service. 
- Wanting reliability pushed me toward containerized deployments, automated workflows, and centralized routing.
- Wanting maintainability led me to organize the work into dedicated application, service, package, and platform repositories.

AI accelerated the development process, but it also made ownership more important. Generated code still had to be understood, validated, integrated, secured, deployed, and maintained. Filling in those gaps became the real purpose of Pior Labs.

The result is no longer just a collection of applications built for a résumé. It is an evolving platform that demonstrates how I approach full-stack development, infrastructure, authentication, automation, system design, and the practical challenges of running software myself.

## Platform

The platform is being standardized around independently deployable services, a shared React design system, centralized authentication, Docker, Caddy, PostgreSQL, GitHub Actions, Tailscale, and Cloudflare.

## Projects

| Repository | Purpose | Status |
| --- | --- | --- |
| [`app-dashboard`](https://github.com/pior-labs/app-dashboard) | Central launchpad for hosted applications | Active |
| [`service-auth`](https://github.com/pior-labs/service-auth) | Shared authentication and SSO | In progress |
| [`package-design-system`](https://github.com/pior-labs/package-design-system) | Shared UI components and design tokens | Active |
| [`platform`](https://github.com/pior-labs/platform) | Public architecture and platform documentation | In progress |
| [`app-finance-tracker`](https://github.com/pior-labs/app-finance-tracker) | Personal finance tracking | Active, migration in progress |
| `app-cookbook` | Recipe collection and meal planning | Planned |
| `app-chatbot` | MCP-enabled platform assistant | Planned |

## Current direction

1. Move application hostnames to `szarans.ca`.
2. Introduce a containerized Caddy edge proxy.
3. Centralize deployment through private platform infrastructure.
4. Deploy the shared authentication service.
5. Migrate existing applications to SSO.
6. Reuse the resulting pattern for future applications.
7. Build more

## Status

Pior Labs is under active development. Planned components and target architecture are marked accordingly.

This is a personal portfolio organization. External pull requests are not currently accepted.
