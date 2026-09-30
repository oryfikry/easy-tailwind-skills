# Install Tailwind CSS with SolidJS

Setting up Tailwind CSS in a SolidJS project.

Source: https://tailwindcss.com/docs/installation/framework-guides/solidjs

## 1. Create your project

Start by creating a new SolidJS project if you don't have one set up already. The most common approach is to use [the SolidJS Vite template](https://www.solidjs.com/guides/getting-started).

**Terminal**

```shell
npx degit solidjs/templates/js my-project
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
import { defineConfig } from 'vite';
import solidPlugin from 'vite-plugin-solid';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [
    tailwindcss(),
    solidPlugin(),
  ],
  server: {
    port: 3000,
  },
  build: {
    target: 'esnext',
  },
});
```

## 4. Import Tailwind CSS

Add an `@import` to `./src/index.css` that imports Tailwind CSS.

**index.css**

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

**App.jsx**

```jsx
export default function App() {
  return (
    <h1 class="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
```
