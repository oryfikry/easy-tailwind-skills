# Installing Tailwind CSS with Vite

Installing Tailwind CSS as a Vite plugin is the most seamless way to integrate it with frameworks like Laravel, SvelteKit, React Router, Nuxt, and SolidJS.

Source: https://tailwindcss.com/docs/installation/using-vite

## 1. Create your project

Start by creating a new Vite project if you don’t have one set up already. The most common approach is to use [Create Vite](https://vite.dev/guide/#scaffolding-your-first-vite-project).

**Terminal**

```shell
npm create vite@latest my-project
cd my-project
```

## 2. Install Tailwind CSS

Install `tailwindcss` and `@tailwindcss/vite` via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/vite
```

## 3. Configure the Vite plugin

Add the `@tailwindcss/vite` plugin to your Vite configuration.

**vite.config.ts**

```js
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})
```

## 4. Import Tailwind CSS

Add an `@import` to your CSS file that imports Tailwind CSS.

**CSS**

```css
@import "tailwindcss";
```

## 5. Start your build process

Run your build process with `npm run dev` or whatever command is configured in your `package.json` file.

**Terminal**

```shell
npm run dev
```

## 6. Start using Tailwind in your HTML

Make sure your compiled CSS is included in the `<head>` *(your framework might handle this for you)*, then start using Tailwind’s utility classes to style your content.

**HTML**

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/src/style.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
