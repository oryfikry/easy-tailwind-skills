# Install Tailwind CSS with Meteor

Setting up Tailwind CSS in a Meteor project.

Source: https://tailwindcss.com/docs/installation/framework-guides/meteor

## 1. Create your project

Start by creating a new Meteor project if you don't have one set up already. The most common approach is to use [the Meteor CLI](https://docs.meteor.com/about/install.html).

**Terminal**

```shell
npx meteor create my-project
cd my-project
```

## 2. Install Tailwind CSS

Install `@tailwindcss/postcss` and its peer dependencies via npm.

**Terminal**

```shell
npm install tailwindcss @tailwindcss/postcss postcss postcss-load-config
```

## 3. Configure PostCSS Plugins

Create a `postcss.config.mjs` file in the root of your project and add the `@tailwindcss/postcss` plugin to your PostCSS configuration.

**postcss.config.mjs**

```js
export default {
  plugins: {
    "@tailwindcss/postcss": {},
  },
};
```

## 4. Import Tailwind CSS

Add an `@import` for Tailwind CSS to your `./client/main.css` file.

**main.css**

```css
@import "tailwindcss";
```

## 5. Start your build process

Run your build process with `npm run start`.

**Terminal**

```shell
npm run start
```

## 6. Start using Tailwind in your project

Start using Tailwind’s utility classes to style your content.

**App.jsx**

```jsx
export const App = () => (
  <h1 className="text-3xl font-bold underline">
    Hello world!
  </h1>
)
```
