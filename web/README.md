# Lodestone web

The Next.js 16 / React 19 web application currently contains the framework starter
page. Its configuration and npm lockfile are part of the Lodestone monorepo.

## Development

Use Node.js 24 LTS and npm. From this directory:

```sh
npm ci
npm run dev
```

Open http://localhost:3000. To verify changes:

```sh
npm run lint
npm run build
```

`npm start` serves an existing production build. Build-time Google font downloads
require network access.

See [web architecture](../docs/architecture/web.md) and the root
[contributing guidelines](../CONTRIBUTING.md) before making changes.
