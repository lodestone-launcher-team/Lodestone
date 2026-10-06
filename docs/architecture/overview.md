# Lodestone architecture

The repository currently contains application scaffolds and empty shared libraries. It establishes build and dependency boundaries; Lodestone product functionality has not been implemented.

## Components

| Path | Current contents |
| --- | --- |
| `src/Lodestone.Desktop` | .NET 10 / Avalonia 12 desktop starter with a single welcome window. |
| `src/Lodestone.Server` | .NET 10 / ASP.NET Core application with development OpenAPI support and HTTPS redirection. No product endpoints. |
| `src/Lodestone.Core` | Empty .NET 10 class library. |
| `src/Lodestone.Minecraft` | Empty .NET 10 class library. |
| `src/Lodestone.Packages` | Empty .NET 10 class library. |
| `tests/` | Three xUnit projects, each referencing its corresponding library; no test cases yet. |
| `web/` | Next.js 16 / React 19 starter using TypeScript, the App Router and Tailwind CSS. |

`Lodestone.slnx` contains the .NET projects. The web application has its own npm toolchain and committed `package-lock.json`.

## Project references

- Desktop references Core, Minecraft and Packages.
- Server references Core and Packages.
- Minecraft and Packages each reference Core.
- Core has no project references.
- Each test project references its corresponding library.
- The web application has no direct .NET project references or implemented backend integration.

Applications may depend on libraries. Libraries must not depend on applications. See [the dependency decision](../decisions/0005-dependency-direction.md).

## Development documentation

- [Desktop](desktop.md)
- [Web](web.md)
- [Architecture decisions](../decisions/0001-use-monorepo.md)
