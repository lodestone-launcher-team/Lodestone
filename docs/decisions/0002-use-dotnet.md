# ADR 0002: Use .NET

Date: 2026-10-06

Status: Accepted

## Context

The existing desktop, ASP.NET Core server, shared libraries and xUnit projects target `net10.0`.

## Decision

Keep C# and .NET 10 for these projects. Maintain their membership in `Lodestone.slnx` and select the SDK with the root `global.json`.

## Consequences

One solution supports restore, build and test for the .NET projects. SDK upgrades must be coordinated with the project targets and CI; the web application keeps its npm toolchain.
