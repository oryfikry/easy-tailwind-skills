# zoom

Utilities for scaling elements using zoom.

Source: https://tailwindcss.com/docs/zoom

| Class | Styles |
| --- | --- |
| `zoom-<number>` | `zoom: <number>%;` |
| `zoom-(<custom-property>)` | `zoom: var(<custom-property>);` |
| `zoom-[<value>]` | `zoom: <value>;` |

## Examples

### Basic example

Use `zoom-<number>` utilities like `zoom-75` and `zoom-125` to scale an element using the CSS `zoom` property:

```html
<div class="zoom-75 ...">
  <!-- ... -->
</div>
<div class="zoom-100 ...">
  <!-- ... -->
</div>
<div class="zoom-125 ...">
  <!-- ... -->
</div>
```

### Using a custom value

Use the `zoom-[<value>]` syntax to set the zoom based on a completely custom value:

```html
<div class="zoom-[1.1] ...">
  <!-- ... -->
</div>
```

For CSS variables, you can also use the `zoom-(<custom-property>)` syntax:

```html
<div class="zoom-(--my-zoom) ...">
  <!-- ... -->
</div>
```

This is just a shorthand for `zoom-[var(<custom-property>)]` that adds the `var()` function for you automatically.

### Applying on hover

Prefix a `zoom` utility with a variant like `hover:*` to only apply the utility in that state:

```html
<div class="zoom-100 hover:zoom-125 ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).

### Responsive design

Prefix a `zoom` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<div class="zoom-100 md:zoom-125 ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
