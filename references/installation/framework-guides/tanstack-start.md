# Install Tailwind CSS with TanStack Start

Setting up Tailwind CSS in a TanStack Start project.

Source: https://tailwindcss.com/docs/installation/framework-guides/tanstack-start

## 1. Create project

Start by creating a new TanStack Start project if you don’t have one set up already. The most common approach is to use [Create Start App](https://tanstack.com/start/latest/docs/framework/react/overview).

**Terminal**

```shell
npx create-start-app@latest my-project
cd my-project
```

## 2. Install Tailwind CSS

Install `@tailwindcss/vite` and its peer dependencies via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/vite
```

## 3. Configure Vite Plugin

Add the `@tailwindcss/vite` plugin to your Vite configuration.

**vite.config.ts**

```ts
import { tanstackStart } from '@tanstack/react-start/plugin/vite';
import { defineConfig } from 'vite';
import tsConfigPaths from 'vite-tsconfig-paths';
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss()
    tanstackStart(),
    tsConfigPaths(),
  ]
});
```

## 4. Import Tailwind CSS

Add an `@import` to `./src/styles.css` that imports Tailwind CSS.

**src/styles.css**

```css
@import "tailwindcss";
```

## 5. Import the CSS file in your root route

Import the CSS file in your `__root.tsx` file with the `?url` query.

**src/routes/__root.tsx**

```tsx
// other imports...

import appCss from '../styles.css?url'

export const Route = createRootRoute({
  head: () => ({
    meta: [
      // your meta tags and site config
    ],
    links: [{ rel: 'stylesheet', href: appCss }],
    // other head config
  }),
  component: RootComponent,
})
```

## 6. Start using Tailwind in your project

Start using Tailwind’s utility classes to style your content.

**src/routes/index.tsx**

```tsx
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/')({
  component: App,
})

function App() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello World!
    </h1>
  )
}
```
