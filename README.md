# iGaming Deck

A responsive Under Maintenance landing page built with Astro, TypeScript, and Tailwind CSS 4. Static output for Cloudflare Pages; no adapter or backend required.

## Local development

Use Node.js 24 LTS (also declared in `.node-version`).

```sh
npm ci
npm run dev
```

## Validate and build

```sh
npm run check
npm run build
npm run preview
```

## GitHub: first push

Run from this project directory. These commands assume the remote repository is empty.

```sh
git init -b main
git add .
git commit -m "Add Astro maintenance landing page"
git remote add origin https://github.com/ietanoox/igd.git
git push -u origin main
```

If the remote already contains a README, license, or other commits, clone it first and copy this project's files into that checkout (excluding `node_modules`, `dist`, and `.astro`) before committing. Do not force push over remote history.

## Cloudflare Pages

Create a Pages project and connect `ietanoox/igd`:

- Production branch: `main`
- Framework preset: Astro
- Build command: `npm run build`
- Build output directory: `dist`
- Root directory: leave blank
- Node.js: 24 (from `.node-version`; optionally set `NODE_VERSION=24`)

Future pushes to `main` trigger production builds.

## Editing and adding pages

- Maintenance content: `src/pages/index.astro`
- Brand: `src/components/Brand.astro`
- Theme, Tailwind import, illustration: `src/styles/global.css`
- Shared HTML metadata: `src/layouts/BaseLayout.astro`
- Add future pages under `src/pages/`; Astro creates their routes automatically.

The geometric illustration is original CSS and uses no external assets or services. Motion respects reduced-motion preferences. The maintenance page includes `noindex, nofollow`; remove or make this configurable in the layout when launching the full website. This static page returns HTTP 200, not an HTTP 503 maintenance response.
