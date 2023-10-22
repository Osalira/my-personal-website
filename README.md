# create-svelte

Everything i need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project
```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

install dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of my app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy my app, i need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
