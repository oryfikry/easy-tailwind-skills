# Install Tailwind CSS with Ruby on Rails

Setting up Tailwind CSS in Ruby on Rails v8+ project.

Source: https://tailwindcss.com/docs/installation/framework-guides/ruby-on-rails

## 1. Create your project

Start by creating a new Rails project if you don't have one set up already. The most common approach is to use the [Rails Command Line](https://guides.rubyonrails.org/command_line.html).

**Terminal**

```shell
rails new my-project
cd my-project
```

## 2. Install Tailwind CSS

Install the `tailwindcss-rails` gem then run the install command to set up Tailwind CSS in your project.

**Terminal**

```shell
bundle add tailwindcss-rails
./bin/rails tailwindcss:install
```

## 3. Start your build process

Run your build process with `./bin/dev`.

**Terminal**

```shell
./bin/dev
```

## 4. Start using Tailwind in your project

Start using Tailwind's utility classes to style your content.

**index.html.erb**

```html
<h1 class="text-3xl font-bold underline">
  Hello world!
</h1>
```
