# ![Lodestone Monorepo Cover](/.github/assets/monorepo_cover.png)

![Issues](https://img.shields.io/github/issues-raw/lodestone-launcher-team/Lodestone?color=c78aff&label=issues&style=for-the-badge)
![Pull Requests](https://img.shields.io/github/issues-pr-raw/lodestone-launcher-team/Lodestone?color=c78aff&label=PRs&style=for-the-badge)
![Contributors](https://img.shields.io/github/contributors/lodestone-launcher-team/Lodestone?color=c78aff&label=contributors&style=for-the-badge)
![Lines of Code](https://img.shields.io/endpoint?url=https%3A%2F%2Floctopus.creeperkatze.dev%2Fgithub%2Flodestone-launcher-team%2FLodestone%2Fbadge&logoColor=white&color=c78aff&style=for-the-badge)
![Commit Activity](https://img.shields.io/github/commit-activity/m/lodestone-launcher-team/Lodestone?color=c78aff&label=commits&style=for-the-badge)
![Last Commit](https://img.shields.io/github/last-commit/lodestone-launcher-team/Lodestone?color=c78aff&label=last%20commit&style=for-the-badge)

## Lodestone Monorepo

Welcome to the Lodestone Monorepo, the primary codebase for the Lodestone desktop launcher, web interface, backend services, and shared libraries. It contains ![Lines of code](https://img.shields.io/endpoint?url=https%3A%2F%2Floctopus.creeperkatze.dev%2Fgithub%2Flodestone-launcher-team%2FLodestone%2Fbadge%3Fformat%3Dhuman&logoColor=white&color=black&label=) lines of code and has ![Contributors](https://img.shields.io/github/contributors/lodestone-launcher-team/Lodestone?color=black&label=) contributors!

Lodestone is a Minecraft launcher and environment manager focused on making Minecraft installations reproducible, portable, and easy to share. If you're not a developer and you've stumbled upon this repository, the public website and application downloads will be available through the Lodestone website once public releases begin.

The current repository is an initial scaffold: an Avalonia desktop application, an ASP.NET Core backend, shared .NET libraries, xUnit project scaffolds, and a Next.js web application. Launcher and environment-management features are not implemented yet.

## Development

This repository contains the primary components of Lodestone. For detailed development information, please refer to their respective documentation:

- [Desktop app](./docs/architecture/desktop.md)
- [Website frontend](./docs/architecture/web.md)
- [Architecture overview](./docs/architecture/overview.md)

Use the .NET SDK selected by `global.json` (10.0.203 with patch roll-forward), Node.js 24 LTS, and npm.

From the repository root:

```sh
dotnet restore
dotnet build
dotnet test
```

From `web/`:

```sh
npm ci
npm run lint
npm run build
```

The xUnit projects currently contain no test cases. GitHub Actions builds and tests the .NET solution and lints and builds the web application. See [contributing guidelines](CONTRIBUTING.md) for the branch workflow.

## Contributing

We welcome contributions! Before submitting any contributions, please read our [contributing guidelines](CONTRIBUTING.md).

If you plan to fork this repository for your own purposes, please review our [copying guidelines](COPYING.md).

## Security

If you discover a security vulnerability within our codebase, please follow our [responsible disclosure guidelines](SECURITY.md).

## Support

If you need help with Lodestone, please visit our support resources once they become available. For general questions, bug reports, and feature requests, you can also use the repository's GitHub issues.

## License

Lodestone's original code and documentation use the [PolyForm Noncommercial License 1.0.0](LICENSE.md). Noncommercial use and contributions are welcome; commercial use requires separate permission. This is a source-available project. See [COPYING.md](COPYING.md) for details. Third-party dependencies retain their own licenses.
