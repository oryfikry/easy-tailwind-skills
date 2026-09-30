# scrollbar-width

Utilities for controlling the width of an element's scrollbar.

Source: https://tailwindcss.com/docs/scrollbar-width

| Class | Styles |
| --- | --- |
| `scrollbar-auto` | `scrollbar-width: auto;` |
| `scrollbar-thin` | `scrollbar-width: thin;` |
| `scrollbar-none` | `scrollbar-width: none;` |

## Examples

### Using the default scrollbar width

Use the `scrollbar-auto` utility to use the browser's default scrollbar width:

```html
<div class="scrollbar-auto overflow-auto ...">
  <!-- ... -->
</div>
```

### Using a thin scrollbar

Use the `scrollbar-thin` utility to use a thinner scrollbar:

```html
<div class="scrollbar-thin overflow-auto ...">
  <!-- ... -->
</div>
```

### Hiding scrollbars

Use the `scrollbar-none` utility to hide scrollbars while still allowing an element to scroll:

```html
<div class="scrollbar-none overflow-auto ...">
  <!-- ... -->
</div>
```

These utilities only support the browser keywords `auto`, `thin`, and `none`.

### Responsive design

Prefix a `scrollbar-width` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<div class="scrollbar-none md:scrollbar-auto ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
