# ADR 0004: Use Next.js

Date: 2026-10-06

Status: Accepted

## Context

The web application is already a Next.js 16 / React 19 starter with TypeScript and the App Router.

## Decision

Retain Next.js and npm for `web/`. Commit `package-lock.json` and use `npm ci` in CI.

## Consequences

Web development and validation use the existing npm scripts. The web application builds independently of the .NET solution; no backend contract, deployment model or product functionality is established yet.
