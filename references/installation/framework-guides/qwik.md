# Install Tailwind CSS with Qwik

Setting up Tailwind CSS in an Qwik project.

Source: https://tailwindcss.com/docs/installation/framework-guides/qwik

## 1. Create your project

Start by creating a new Qwik project if you don't have one set up already. The most common approach is to use [Create Qwik](https://qwik.dev/docs/getting-started/#create-an-app-using-the-cli).

**Terminal**

```shell
npm create qwik@latest empty my-project
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
import { defineConfig } from 'vite'
import { qwikVite } from "@builder.io/qwik/optimizer";
import { qwikCity } from "@builder.io/qwik-city/vite";
// …

import tailwindcss from '@tailwindcss/vite'

export default defineConfig(({ command, mode }): UserConfig => {
  return {
    plugins: [
      tailwindcss(),
      qwikCity(),
      qwikVite(),
      tsconfigPaths(),
    ],

    // …
  }
})
```

## 4. Import Tailwind CSS

Add an `@import` to `./src/global.css` that imports Tailwind CSS.

**global.css**

```css
@import "tailwindcss";
```

## 5. Start your build process

Run your build process with `npm run dev`.

**Terminal**

```shell
npm run dev
```

## 6. Start using Tailwind in your project

Start using Tailwind’s utility classes to style your content.

**index.tsx**

```tsx
import { component$ } from '@builder.io/qwik'

export default component$(() => {
  return (
    <h1 class="text-3xl font-bold underline">
      Hello World!
    </h1>
  )
})
```
