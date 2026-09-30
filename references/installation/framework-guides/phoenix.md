# Install Tailwind CSS with Phoenix

Setting up Tailwind CSS in a Phoenix project.

Source: https://tailwindcss.com/docs/installation/framework-guides/phoenix

## 1. Create your project

Start by creating a new Phoenix project if you don't have one set up already. You can follow their [installation guide](https://hexdocs.pm/phoenix/installation.html) to get up and running.

**Terminal**

```shell
mix phx.new myproject
cd myproject
```

## 2. Install the Tailwind plugin

Add the Tailwind plugin to your dependencies and run `mix deps.get` to install it.

**mix.exs**

```elixir
defp deps do
  [
    # …
    {:tailwind, "~> 0.3", runtime: Mix.env() == :dev},
  ]
end
```

## 3. Configure the Tailwind plugin

In your `config/config.exs` file you can set which version of Tailwind CSS you want to use and customize your asset paths.

**config.exs**

```elixir
config :tailwind,
  version: "4.1.10",
  myproject: [
    args: ~w(
      --input=assets/css/app.css
      --output=priv/static/assets/app.css
    ),
    cd: Path.expand("..", __DIR__)
  ]
```

## 4. Update your deployment script

Configure your `assets.deploy` alias to build your CSS on deployment.

**mix.exs**

```elixir
defp aliases do
  [
    # …
    "assets.deploy": [
      "tailwind myproject --minify",
      "esbuild myproject --minify",
      "phx.digest"
    ]
  ]
end
```

## 5. Enable watcher in development

Add Tailwind to your list of watchers in your `./config/dev.exs` file.

**dev.exs**

```elixir
watchers: [
  # Start the esbuild watcher by calling Esbuild.install_and_run(:default, args)
  esbuild: {Esbuild, :install_and_run, [:myproject, ~w(--sourcemap=inline --watch)]},
  tailwind: {Tailwind, :install_and_run, [:myproject, ~w(--watch)]}
]
```

## 6. Install Tailwind CSS

Run the install command to download the standalone Tailwind CLI.

**Terminal**

```shell
mix tailwind.install
```

## 7. Import Tailwind CSS

Add an `@import` to `./assets/css/app.css` that imports Tailwind CSS.

**app.css**

```css
@import "tailwindcss";
```

## 8. Remove the default CSS import

Remove the CSS import from `./assets/js/app.js`, as Tailwind is now handling this for you.

**app.js**

```js
- // Remove this line if you add your own CSS build pipeline (e.g postcss).
- import "../css/app.css"
```

## 9. Start your build process

Run your build process with `mix phx.server`.

**Terminal**

```shell
mix phx.server
```

## 10. Start using Tailwind in your project

Start using Tailwind’s utility classes to style your content.

**index.html.heex**

```html
<h1 class="text-3xl font-bold underline">
  Hello world!
</h1>
```
