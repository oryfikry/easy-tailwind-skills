# Install Tailwind CSS with AdonisJS

Setting up Tailwind CSS in an AdonisJS project.

Source: https://tailwindcss.com/docs/installation/framework-guides/adonisjs

## 1. Create your project

Start by creating a new AdonisJS project if you don’t have one set up already. The most common approach is to use [Create AdonisJS](https://docs.adonisjs.com/guides/getting-started/installation).

**Terminal**

```shell
npm init adonisjs@latest my-project -- --kit=web
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
import adonisjs from '@adonisjs/vite/client'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
    adonisjs({
      // …
    }),
  ],
})
```

## 4. Import Tailwind CSS

Add an `@import` to `./resources/css/app.css` that imports Tailwind CSS's styles. Additionally, tell Tailwind CSS to scan your `resources/views` directory for utilities.

**app.css**

```css
@import "tailwindcss";
@source "../views";
```

## 5. Start your build process

Run your build process with `npm run dev`.

## 6. Start using Tailwind in your project

Make sure your compiled CSS is included in the `<head>` then start using Tailwind’s utility classes to style your content.

**home.edge**

```edge
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    @vite(['resources/css/app.css', 'resources/js/app.js'])
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">
      Hello world!
    </h1>
  </body>
</html>
```
