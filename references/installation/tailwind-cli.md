# Tailwind CLI

The simplest and fastest way to get up and running with Tailwind CSS from scratch is with the Tailwind CLI tool. The CLI is also available as a standalone executable if you want to use it without installing Node.js.

Source: https://tailwindcss.com/docs/installation/tailwind-cli

## 1. Install Tailwind CSS

Install `tailwindcss` and `@tailwindcss/cli` via npm.

## 2. Import Tailwind in your CSS

Add the `@import "tailwindcss";` import to your main CSS file.

## 3. Start the Tailwind CLI build process

Run the CLI tool to scan your source files for classes and build your CSS.

## 4. Start using Tailwind in your HTML

Add your compiled CSS file to the `<head>` and start using Tailwind’s utility classes to style your content.

**src/index.html**

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
