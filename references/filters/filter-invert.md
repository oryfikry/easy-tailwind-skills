# filter: invert()

Utilities for applying invert filters to an element.

Source: https://tailwindcss.com/docs/filter-invert

| Class | Styles |
| --- | --- |
| `invert` | `filter: invert(100%);` |
| `invert-<number>` | `filter: invert(<number>%);` |
| `invert-(<custom-property>)` | `filter: invert(var(<custom-property>));` |
| `invert-[<value>]` | `filter: invert(<value>);` |

## Examples

### Basic example

Use utilities like `invert` and `invert-20` to control the color inversion of an element:

```html
<img class="invert-0" src="/img/mountains.jpg" />
<img class="invert-20" src="/img/mountains.jpg" />
<img class="invert" src="/img/mountains.jpg" />
```

### Using a custom value

Use the `invert-[<value>]` syntax to set the color inversion based on a completely custom value:

```html
<img class="invert-[.25] ..." src="/img/mountains.jpg" />
```

For CSS variables, you can also use the `invert-(<custom-property>)` syntax:

```html
<img class="invert-(--my-inversion) ..." src="/img/mountains.jpg" />
```

This is just a shorthand for `invert-[var(<custom-property>)]` that adds the `var()` function for you automatically.

### Responsive design

Prefix a `filter: invert()` utility with a breakpoint variant like `md:` to only apply the utility at medium screen sizes and above:

```html
<img class="invert md:invert-0 ..." src="/img/mountains.jpg" />
```

Learn more about using variants in the [variants documentation](../core-concepts/hover-focus-and-other-states.md).
