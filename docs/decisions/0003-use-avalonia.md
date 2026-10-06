# ADR 0003: Use Avalonia

Date: 2026-10-06

Status: Accepted

## Context

The desktop project is already an Avalonia 12 starter with a XAML window and Fluent theme.

## Decision

Retain Avalonia for the desktop application and preserve the framework startup, XAML resources and application manifest.

## Consequences

Desktop UI changes will use the existing Avalonia project. It currently contains only the welcome window; this decision does not specify launcher behavior or a future UI design.
