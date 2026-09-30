# Install Tailwind CSS with Laravel

Setting up Tailwind CSS in a Laravel project.

Source: https://tailwindcss.com/docs/installation/framework-guides/laravel

## 1. Create your project

Start by creating a new Laravel project if you don’t have one set up already. The most common approach is to use [the Laravel installer](https://laravel.com/docs#creating-an-application).

**Terminal**

```shell
laravel new my-project
cd my-project
```

## 2. Install Tailwind CSS

Install `@tailwindcss/vite` and its peer dependencies via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/vite
```

## 3. Install Tailwind CSS

Install `@tailwindcss/postcss` and its peer dependencies via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/postcss postcss
```

## 4. Configure Vite Plugin

Add the `@tailwindcss/vite` plugin to your Vite configuration.

**vite.config.ts**

```ts
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
    // …
  ],
})
```

## 5. Add Tailwind to your Laravel Mix configuration

In your `webpack.mix.js` file, add `tailwindcss` as a PostCSS plugin.

**webpack.mix.js**

```js
mix
  .js("resources/js/app.js", "public/js")
  .postCss("resources/css/app.css", "public/css", [
    require("@tailwindcss/postcss"),
  ]);
```

## 6. Import Tailwind CSS

Add an `@import` to `./resources/css/app.css` that imports Tailwind CSS. Additionally, tell Tailwind CSS to scan some directories for utilities.

**app.css**

```css
@import "tailwindcss";

@source "../../vendor/laravel/framework/src/Illuminate/Pagination/resources/views/*.blade.php";
@source "../../storage/framework/views/*.php";
@source "../**/*.blade.php";
@source "../**/*.js";
```

## 7. Start your build process

Run your build process with `npm run dev`.

**Terminal**

```shell
npm run dev
```

## 8. Start your build process

Run your build process with `npm run watch`.

**Terminal**

```shell
npm run watch
```

## 9. Start using Tailwind in your project

Make sure your compiled CSS is included in the `<head>` then start using Tailwind’s utility classes to style your content.

**app.blade.php**

```blade
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    @vite('resources/css/app.css')
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">
      Hello world!
    </h1>
  </body>
</html>
```

## 10. Start using Tailwind in your project

Make sure your compiled CSS is included in the `<head>` then start using Tailwind’s utility classes to style your content.

**app.blade.php**

```blade
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="{{ asset('css/app.css') }}" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">
      Hello world!
    </h1>
  </body>
</html>
```
