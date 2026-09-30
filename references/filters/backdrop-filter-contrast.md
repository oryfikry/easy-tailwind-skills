# backdrop-filter: contrast()

Utilities for applying backdrop contrast filters to an element.

Source: https://tailwindcss.com/docs/backdrop-filter-contrast

| Class | Styles |
| --- | --- |
| `backdrop-contrast-<number>` | `backdrop-filter: contrast(<number>%);` |
| `backdrop-contrast-(<custom-property>)` | `backdrop-filter: contrast(var(<custom-property>));` |
| `backdrop-contrast-[<value>]` | `backdrop-filter: contrast(<value>);` |

## Examples

### Basic example

Use utilities like `backdrop-contrast-50` and `backdrop-contrast-100` to control an element's backdrop contrast:

```html
<div class="bg-[url(/img/mountains.jpg)]">
  <div class="bg-white/30 backdrop-contrast-50 ..."></div>
</div>
<div class="bg-[url(/img/mountains.jpg)]">
  <div class="bg-white/30 backdrop-contrast-200 ..."></div>
</div>
```

### Using a custom value

Use the `backdrop-contrast-[<value>]` syntax to set the backdrop contrast based on a completely custom value:

```html
<div class="backdrop-contrast-[.25] ...">
  <!-- ... -->
</div>
```

For CSS variables, you can also use the `backdrop-contrast-(<custom-property>)` syntax:

```html
<div class="backdrop-contrast-(--my-backdrop-contrast) ...">
  <!-- ... -->
</div>
```

This is just a shorthand for `backdrop-contrast-[var(<custom-property>)]` that adds the `var()` function for you automatically.

### Responsive design

Prefix a `backdrop-filter: contrast()` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<div class="backdrop-contrast-125 md:backdrop-contrast-150 ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
