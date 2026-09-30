# Install Tailwind CSS with Symfony

Setting up Tailwind CSS in a Symfony project.

Source: https://tailwindcss.com/docs/installation/framework-guides/symfony

## 1. Create your project

Start by creating a new Symfony project if you don’t have one set up already. The most common approach is to use [the Symfony Installer](https://symfony.com/download).

**Terminal**

```shell
symfony new --webapp my-project
cd my-project
```

## 2. Install Webpack Encore

Install Webpack Encore, which handles building your assets. See [the documentation](https://symfony.com/doc/current/frontend.html) for more information.

**Terminal**

```shell
composer remove symfony/ux-turbo symfony/asset-mapper symfony/stimulus-bundle
composer require symfony/webpack-encore-bundle symfony/ux-turbo symfony/stimulus-bundle
```

## 3. Install Tailwind CSS

Using npm, install `@tailwindcss/postcss` and its peer dependencies, as well as `postcss-loader`.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/postcss postcss postcss-loader
```

## 4. Enable PostCSS support

In your `webpack.config.js` file, enable the PostCSS Loader. See [the documentation](https://symfony.com/doc/current/frontend/encore/postcss.html) for more information.

**webpack.config.js**

```js
Encore
  .enablePostCssLoader()
;
```

## 5. Configure PostCSS Plugins

Create a `postcss.config.mjs` file in the root of your project and add the `@tailwindcss/postcss` plugin to your PostCSS configuration.

**postcss.config.mjs**

```js
export default {
  plugins: {
    "@tailwindcss/postcss": {},
  },
};
```

## 6. Import Tailwind CSS

Add an `@import` to `./assets/styles/app.css` that imports Tailwind CSS and an `@source` that ignores the public dir to prevent recompile loops in watch mode.

**app.css**

```css
@import "tailwindcss";
@source not "../../public";
```

## 7. Start your build process

Run your build process with `npm run watch`.

**Terminal**

```shell
npm run watch
```

## 8. Start using Tailwind in your project

Make sure your compiled CSS is included in the `<head>` then start using Tailwind’s utility classes to style your content.

**base.html.twig**

```twig
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0"
    />
    {% block stylesheets %}
      {{ encore_entry_link_tags('app') }}
    {% endblock %}
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">
      Hello world!
    </h1>
  </body>
</html>
```
