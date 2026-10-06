# Web application

`web/` is a Next.js 16 / React 19 starter using TypeScript, the App Router and Tailwind CSS 4. `app/page.tsx` contains the starter page, `app/layout.tsx` defines its layout, and `app/globals.css` holds global styles. No Lodestone web features or backend integration are implemented.

Use the Node.js version selected by the web CI workflow and npm. From `web/`:

```sh
npm ci
npm run dev
```

Open `http://localhost:3000` to view the development server. To validate changes:

```sh
npm run lint
npm run build
```

`npm start` serves a completed production build. Commit `package-lock.json` with dependency changes so local development and CI use the same dependency resolution.

See [the architecture overview](overview.md) and [the Next.js decision](../decisions/0004-use-nextjs.md).
