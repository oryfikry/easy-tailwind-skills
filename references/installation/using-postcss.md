# Installing Tailwind CSS with PostCSS

Installing Tailwind CSS as a PostCSS plugin is the most seamless way to integrate it with frameworks like Next.js and Angular.

Source: https://tailwindcss.com/docs/installation/using-postcss

## 1. Install Tailwind CSS

Install `tailwindcss`, `@tailwindcss/postcss`, and `postcss` via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/postcss postcss
```

## 2. Add Tailwind to your PostCSS configuration

Add `@tailwindcss/postcss` to your `postcss.config.mjs` file, or wherever PostCSS is configured in your project.

**postcss.config.mjs**

```js
export default {
  plugins: {
    "@tailwindcss/postcss": {},
  }
}
```

## 3. Import Tailwind CSS

Add an `@import` to your CSS file that imports Tailwind CSS.

**CSS**

```css
@import "tailwindcss";
```

## 4. Start your build process

Run your build process with `npm run dev` or whatever command is configured in your `package.json` file.

**Terminal**

```shell
npm run dev
```

## 5. Start using Tailwind in your HTML

Make sure your compiled CSS is included in the `<head>` *(your framework might handle this for you)*, then start using Tailwind’s utility classes to style your content.

**HTML**

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/styles.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
