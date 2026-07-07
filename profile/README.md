# Pior Labs

Pior Labs is a self-hosted software platform and engineering portfolio. It brings together full-stack applications, shared services, reusable packages, and the infrastructure used to operate them as one coherent system.

## Platform

The platform is being standardized around independently deployable services, a shared React design system, centralized authentication, Docker, Caddy, PostgreSQL, GitHub Actions, Tailscale, and Cloudflare.

## Projects

| Repository | Purpose | Status |
| --- | --- | --- |
| [`app-dashboard`](https://github.com/pior-labs/app-dashboard) | Central launchpad for hosted applications | Active |
| [`service-auth`](https://github.com/pior-labs/service-auth) | Shared authentication and SSO | In progress |
| [`package-design-system`](https://github.com/pior-labs/package-design-system) | Shared UI components and design tokens | Active |
| [`platform`](https://github.com/pior-labs/platform) | Public architecture and platform documentation | In progress |
| `app-finance-tracker` | Personal finance tracking | Active, migration in progress |
| `app-cookbook` | Recipe collection and meal planning | Planned |
| `app-chatbot` | MCP-enabled platform assistant | Planned |

## Current direction

1. Move application hostnames to `szarans.ca`.
2. Introduce a containerized Caddy edge proxy.
3. Centralize deployment through private platform infrastructure.
4. Deploy the shared authentication service.
5. Migrate existing applications to SSO.
6. Reuse the resulting pattern for future applications.

## Status

Pior Labs is under active development. Planned components and target architecture are marked accordingly.

This is a personal portfolio organization. External pull requests are not currently accepted.
