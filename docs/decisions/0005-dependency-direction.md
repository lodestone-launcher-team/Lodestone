# ADR 0005: Keep dependencies directed toward libraries

Date: 2026-10-06

Status: Accepted

## Context

The existing project references place shared libraries below the applications. Core has no project references; Minecraft and Packages each reference Core.

## Decision

Keep application-to-library dependencies. Desktop references Core, Minecraft and Packages; Server references Core and Packages. Libraries must not reference applications. Each test project references its corresponding library.

The web application remains a separate npm project with no direct .NET project references.

## Consequences

Shared libraries can be built and tested without either application. New references must preserve this direction and avoid cycles. Future cross-application integration requires a separate decision once its requirements are known.
