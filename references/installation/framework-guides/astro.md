# Install Tailwind CSS with Astro

Setting up Tailwind CSS in an Astro project.

Source: https://tailwindcss.com/docs/installation/framework-guides/astro

## 1. Create your project

Start by creating a new Astro project if you don't have one set up already. The most common approach is to use [create astro](https://docs.astro.build/en/install-and-setup/#install-from-the-cli-wizard).

**Terminal**

```shell
npm create astro@latest my-project
cd my-project
```

## 2. Install Tailwind CSS

Install `@tailwindcss/vite` and its peer dependencies via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/vite
```

## 3. Configure Vite Plugin

Add the `@tailwindcss/vite` plugin to your Vite plugins in your Astro config file.

**astro.config.mjs**

```js
// @ts-check
import { defineConfig } from "astro/config";
import tailwindcss from "@tailwindcss/vite";

// https://astro.build/config
export default defineConfig({
  vite: {
    plugins: [tailwindcss()],
  },
});
```

## 4. Import Tailwind CSS

Create a `./src/styles/global.css` file and add an `@import` for Tailwind CSS.

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

Start using Tailwind's utility classes to style your content while making sure to import the newly created CSS file.

**index.astro**

```astro
---
import "../styles/global.css";
---

<h1 class="text-3xl font-bold underline">
  Hello world!
</h1>
```
