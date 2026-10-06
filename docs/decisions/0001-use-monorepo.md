# ADR 0001: Use a monorepo

Date: 2026-10-06

Status: Accepted

## Context

The desktop application, server, shared .NET libraries, test projects and web application already live in one repository.

## Decision

Keep this structure. Place .NET application and library projects in `src/`, tests in `tests/`, the Next.js application in `web/`, and documentation in `docs/`.

## Consequences

Related changes can be reviewed together. The .NET solution and npm application retain separate build commands and CI workflows.
