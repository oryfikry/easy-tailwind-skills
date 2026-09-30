# list-style-position

Utilities for controlling the position of bullets and numbers in lists.

Source: https://tailwindcss.com/docs/list-style-position

| Class | Styles |
| --- | --- |
| `list-inside` | `list-style-position: inside;` |
| `list-outside` | `list-style-position: outside;` |

## Examples

### Basic example

Use utilities like `list-inside` and `list-outside` to control the position of the markers and text indentation in a list:

```html
<ul class="list-inside">
  <li>5 cups chopped Porcini mushrooms</li>
  <!-- ... -->
</ul>

<ul class="list-outside">
  <li>5 cups chopped Porcini mushrooms</li>
  <!-- ... -->
</ul>
```

### Responsive design

Prefix a `list-style-position` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<ul class="list-outside md:list-inside ...">
  <!-- ... -->
</ul>
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
