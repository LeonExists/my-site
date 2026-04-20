# Vue + Bun Site Template

A minimal, ready-to-clone template for building multi-page sites with Vue 3, Vue Router, and Bun. Deploys automatically to GitHub Pages on every push to `main`.

## Project structure

```
src/
├── assets/          # Global CSS and static files
├── components/
│   └── layout/      # App-wide layout components (header, footer, etc.)
├── views/           # One file per page/route
├── router/          # Vue Router config (index.js)
├── App.vue          # Root component — mounts layout + <RouterView>
└── main.js          # App entry point
```

Add new pages by creating a file in `views/` and registering it in `router/index.js`.

## Setup

```sh
bun install
```

## Development

```sh
bun dev
```

## Build

```sh
bun run build
```

## Deploy

Pushing to `main` automatically builds and deploys to GitHub Pages via GitHub Actions.

> **First-time setup:** Go to your repo **Settings → Pages** and set **Source** to **GitHub Actions**.
>
> **Repo name:** If your GitHub repo is not named `my-site`, update the `base` field in `vite.config.js` to match — e.g. `base: '/your-repo-name/'`.

## Tech

- [Vue 3](https://vuejs.org/) with `<script setup>`
- [Vue Router 5](https://router.vuejs.org/) (hash history — works on any static host)
- [Vite 8](https://vite.dev/)
- [Bun](https://bun.sh/)
- GitHub Actions for CI/CD
