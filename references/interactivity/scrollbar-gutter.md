# scrollbar-gutter

Utilities for controlling the gutter space reserved for an element's scrollbar.

Source: https://tailwindcss.com/docs/scrollbar-gutter

| Class | Styles |
| --- | --- |
| `scrollbar-gutter-auto` | `scrollbar-gutter: auto;` |
| `scrollbar-gutter-stable` | `scrollbar-gutter: stable;` |
| `scrollbar-gutter-both` | `scrollbar-gutter: stable both-edges;` |

## Examples

### Reserving space for the scrollbar

Use the `scrollbar-gutter-stable` utility to reserve space for the scrollbar even when an element isn't overflowing:

```html
<div class="scrollbar-gutter-stable overflow-auto ...">
  <!-- ... -->
</div>
```

### Reserving space on both sides

Use the `scrollbar-gutter-both` utility to reserve matching gutter space on both sides of the element:

```html
<div class="scrollbar-gutter-both overflow-auto ...">
  <!-- ... -->
</div>
```

### Using the default gutter

Use the `scrollbar-gutter-auto` utility to only reserve gutter space when the browser would normally show a scrollbar:

```html
<div class="scrollbar-gutter-auto overflow-auto ...">
  <!-- ... -->
</div>
```

### Responsive design

Prefix a `scrollbar-gutter` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<div class="scrollbar-gutter-auto md:scrollbar-gutter-stable ...">
  <!-- ... -->
</div>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
