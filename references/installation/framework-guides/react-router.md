# Install Tailwind CSS with React Router

Setting up Tailwind CSS in a React Router project.

Source: https://tailwindcss.com/docs/installation/framework-guides/react-router

## 1. Create your project

Start by creating a new React Router project if you don’t have one set up already. The most common approach is to use [Create React Router](https://reactrouter.com/start/framework/installation).

**Terminal**

```shell
npx create-react-router@latest my-project
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
import { reactRouter } from "@react-router/dev/vite";
import { defineConfig } from "vite";
import tsconfigPaths from "vite-tsconfig-paths";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [
    tailwindcss(),
    reactRouter(),
    tsconfigPaths(),
  ],
});
```

## 4. Import Tailwind CSS

Add an `@import` to `./app/app.css` that imports Tailwind CSS.

**app.css**

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

**home.tsx**

```tsx
export default function Home() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
```
