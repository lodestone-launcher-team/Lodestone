# Contributing to Lodestone

Issues and pull requests are welcome. The repository currently contains project
scaffolds; discuss substantial work in an issue before starting it.

## Permissions

Read [LICENSE.md](LICENSE.md) and [COPYING.md](COPYING.md) first. Noncommercial
contributions are permitted. Commercial use requires separate permission.
By submitting code or documentation, you confirm that you have permission to
contribute it and provide it under the repository's license. Contributors retain
copyright in their contributions. Identify any third-party material and its license.

## Set up and verify

Use the .NET SDK selected by `global.json` (10.0.203, allowing newer patches in
the same feature band), Node.js 24 LTS, and npm.

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

The three xUnit projects are empty scaffolds at bootstrap. A successful test
command currently confirms the test projects build and load; it does not verify
product behavior. Add meaningful tests when behavior is implemented.

## Pull requests

`main` is the stable branch. Bootstrap work uses `chore/repository-bootstrap`.
After the bootstrap PR is merged, the intended model is `feature/*` into `dev`,
then `dev` into `main`. Until `dev` exists, target `main`.

Keep changes focused, explain the problem and resulting behavior, update related
documentation, and list verification results. Follow existing style and project
references; see [architecture](docs/architecture/overview.md).

Commit source files and `web/package-lock.json`. Keep credentials, local environment
files, IDE settings, and generated build output out of Git. Report vulnerabilities
through [SECURITY.md](SECURITY.md).
