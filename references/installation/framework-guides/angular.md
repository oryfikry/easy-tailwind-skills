# Install Tailwind CSS with Angular

Setting up Tailwind CSS in an Angular project.

Source: https://tailwindcss.com/docs/installation/framework-guides/angular

## 1. Create your project

Start by creating a new Angular project if you don’t have one set up already. The most common approach is to use [Angular CLI](https://angular.dev/tools/cli/setup-local).

**Terminal**

```shell
ng new my-project --style css
cd my-project
```

## 2. Install Tailwind CSS

Install `@tailwindcss/postcss` and its peer dependencies via npm.

), // NOTE: The `--force` flag is used to make sure the installation succeeds. Angular has a peer dependency on `tailwindcss` v3 which causes errors when installing `tailwindcss` v4.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/postcss postcss --force
```

## 3. Configure PostCSS Plugins

Create a `.postcssrc.json` file in the root of your project and add the `@tailwindcss/postcss` plugin to your PostCSS configuration.

**.postcssrc.json**

```js
{
  "plugins": {
    "@tailwindcss/postcss": {}
  }
}
```

## 4. Import Tailwind CSS

Add an `@import` to `./src/styles.css` that imports Tailwind CSS.

**styles.css**

```css
@import "tailwindcss";
```

## 5. Start your build process

Run your build process with `ng serve`.

**Terminal**

```shell
ng serve
```

## 6. Start using Tailwind in your project

Start using Tailwind’s utility classes to style your content.

**app.component.html**

```html
<h1 class="text-3xl font-bold underline">
  Hello world!
</h1>
```
