# outline-width

Utilities for controlling the width of an element's outline.

Source: https://tailwindcss.com/docs/outline-width

| Class | Styles |
| --- | --- |
| `outline` | `outline-width: 1px;` |
| `outline-<number>` | `outline-width: <number>px;` |
| `outline-(length:<custom-property>)` | `outline-width: var(<custom-property>);` |
| `outline-[<value>]` | `outline-width: <value>;` |

## Examples

### Basic example

Use `outline` or `outline-<number>` utilities like `outline-2` and `outline-4` to set the width of an element's outline:

```html
<button class="outline outline-offset-2 ...">Button A</button>
<button class="outline-2 outline-offset-2 ...">Button B</button>
<button class="outline-4 outline-offset-2 ...">Button C</button>
```

### Applying on focus

Prefix an `outline-width` utility with a variant like `focus:*` to only apply the utility in that state:

```html
<button class="outline-offset-2 outline-sky-500 focus:outline-2 ...">Save Changes</button>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).

### Using a custom value

Use the `outline-[<value>]` syntax to set the outline width based on a completely custom value:

```html
<div class="outline-[2vw] ...">
  <!-- ... -->
</div>
```

For CSS variables, you can also use the `outline-(length:<custom-property>)` syntax:

```html
<div class="outline-(length:--my-outline-width) ...">
  <!-- ... -->
</div>
```

This is just a shorthand for `outline-[length:var(<custom-property>)]` that adds the `var()` function for you automatically.

### Responsive design

Prefix an `outline-width` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<div class="outline md:outline-2 ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
