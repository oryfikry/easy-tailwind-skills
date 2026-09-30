---
name: tailwindcss-docs
description: Offline Tailwind CSS v4 documentation split into one markdown file per page (core concepts, base styles, every utility category, installation and framework guides). Use when writing, reviewing or debugging Tailwind classes, variants (hover, responsive, dark), @theme / @utility / @variant / @apply, arbitrary values, colors, or installing Tailwind in Vite, PostCSS or a framework.
---

# Tailwind CSS v4 docs

Converted from the official docs source (github.com/tailwindlabs/tailwindcss.com, `main`, fetched 2026-09-30). One page per file under `references/`, grouped like the docs sidebar.

## How to use

1. Find the page in the index below by utility name (e.g. `padding`, `grid-template-columns`) or concept.
2. Read only that file. Each utility page opens with a class → CSS table, then examples.
3. For variants (`hover:`, `md:`, `dark:`, `group-*`, `has-*`) read `references/core-concepts/hover-focus-and-other-states.md`, `responsive-design.md` and `dark-mode.md`.
4. For customization (`@theme`, `@utility`, `@variant`, `@source`, arbitrary values) read `adding-custom-styles.md`, `theme.md` and `functions-and-directives.md`.

## Conventions in these files

- Rendered demos from the website are removed; every code sample is kept.
- `**name**` above a code block is that block's filename or tab label.
- A `diff` block marks lines the docs show as removed (`-`) and added (`+`).
- Links between pages are relative, so they work from any location.
- `references/core-concepts/default-theme.css` is the full default theme: fonts, colors, spacing, breakpoints, shadows, easings.

## Index

### Getting started

- [Installation](references/getting-started/installation.md) — Install Tailwind CSS with Vite, PostCSS, the CLI, or a CDN, plus 19 framework guides.
- [Editor setup](references/getting-started/editor-setup.md) — Tooling to improve the developer experience when working with Tailwind CSS.
- [Compatibility](references/getting-started/compatibility.md) — Learn about browser support and compatibility with other tooling.
- [Upgrade guide](references/getting-started/upgrade-guide.md) — Upgrading your Tailwind CSS projects from v3 to v4.

### Core concepts

- [Styling with utility classes](references/core-concepts/styling-with-utility-classes.md) — Building complex components from a constrained set of primitive utilities.
- [Hover, focus, and other states](references/core-concepts/hover-focus-and-other-states.md) — Using utilities to style elements on hover, focus, and more.
- [Responsive design](references/core-concepts/responsive-design.md) — Using responsive utility variants to build adaptive user interfaces.
- [Dark mode](references/core-concepts/dark-mode.md) — Using variants to style your site in dark mode.
- [Theme variables](references/core-concepts/theme.md) — Using utility classes as an API for your design tokens.
- [Colors](references/core-concepts/colors.md) — Using and customizing the color palette in Tailwind CSS projects.
- [Adding custom styles](references/core-concepts/adding-custom-styles.md) — Best practices for adding your own custom styles in Tailwind projects.
- [Detecting classes in source files](references/core-concepts/detecting-classes-in-source-files.md) — Understanding and customizing how Tailwind scans your source files.
- [Functions and directives](references/core-concepts/functions-and-directives.md) — A reference for the custom functions and directives Tailwind exposes to your CSS.

### Base styles

- [Preflight](references/base-styles/preflight.md) — An opinionated set of base styles for Tailwind projects.

### Layout

- [aspect-ratio](references/layout/aspect-ratio.md) — Utilities for controlling the aspect ratio of an element.
- [columns](references/layout/columns.md) — Utilities for controlling the number of columns within an element.
- [break-after](references/layout/break-after.md) — Utilities for controlling how a column or page should break after an element.
- [break-before](references/layout/break-before.md) — Utilities for controlling how a column or page should break before an element.
- [break-inside](references/layout/break-inside.md) — Utilities for controlling how a column or page should break within an element.
- [box-decoration-break](references/layout/box-decoration-break.md) — Utilities for controlling how element fragments should be rendered across multiple lines, columns, or pages.
- [box-sizing](references/layout/box-sizing.md) — Utilities for controlling how the browser should calculate an element's total size.
- [display](references/layout/display.md) — Utilities for controlling the display box type of an element.
- [float](references/layout/float.md) — Utilities for controlling the wrapping of content around an element.
- [clear](references/layout/clear.md) — Utilities for controlling the wrapping of content around an element.
- [isolation](references/layout/isolation.md) — Utilities for controlling whether an element should explicitly create a new stacking context.
- [object-fit](references/layout/object-fit.md) — Utilities for controlling how a replaced element's content should be resized.
- [object-position](references/layout/object-position.md) — Utilities for controlling how a replaced element's content should be positioned within its container.
- [overflow](references/layout/overflow.md) — Utilities for controlling how an element handles content that is too large for the container.
- [overscroll-behavior](references/layout/overscroll-behavior.md) — Utilities for controlling how the browser behaves when reaching the boundary of a scrolling area.
- [position](references/layout/position.md) — Utilities for controlling how an element is positioned in the document.
- [top / right / bottom / left](references/layout/top-right-bottom-left.md) — Utilities for controlling the placement of positioned elements.
- [visibility](references/layout/visibility.md) — Utilities for controlling the visibility of an element.
- [z-index](references/layout/z-index.md) — Utilities for controlling the stack order of an element.

### Flexbox & Grid

- [flex-basis](references/flexbox-and-grid/flex-basis.md) — Utilities for controlling the initial size of flex items.
- [flex-direction](references/flexbox-and-grid/flex-direction.md) — Utilities for controlling the direction of flex items.
- [flex-wrap](references/flexbox-and-grid/flex-wrap.md) — Utilities for controlling how flex items wrap.
- [flex](references/flexbox-and-grid/flex.md) — Utilities for controlling how flex items both grow and shrink.
- [flex-grow](references/flexbox-and-grid/flex-grow.md) — Utilities for controlling how flex items grow.
- [flex-shrink](references/flexbox-and-grid/flex-shrink.md) — Utilities for controlling how flex items shrink.
- [order](references/flexbox-and-grid/order.md) — Utilities for controlling the order of flex and grid items.
- [grid-template-columns](references/flexbox-and-grid/grid-template-columns.md) — Utilities for specifying the columns in a grid layout.
- [grid-column](references/flexbox-and-grid/grid-column.md) — Utilities for controlling how elements are sized and placed across grid columns.
- [grid-template-rows](references/flexbox-and-grid/grid-template-rows.md) — Utilities for specifying the rows in a grid layout.
- [grid-row](references/flexbox-and-grid/grid-row.md) — Utilities for controlling how elements are sized and placed across grid rows.
- [grid-auto-flow](references/flexbox-and-grid/grid-auto-flow.md) — Utilities for controlling how elements in a grid are auto-placed.
- [grid-auto-columns](references/flexbox-and-grid/grid-auto-columns.md) — Utilities for controlling the size of implicitly-created grid columns.
- [grid-auto-rows](references/flexbox-and-grid/grid-auto-rows.md) — Utilities for controlling the size of implicitly-created grid rows.
- [gap](references/flexbox-and-grid/gap.md) — Utilities for controlling gutters between grid and flexbox items.
- [justify-content](references/flexbox-and-grid/justify-content.md) — Utilities for controlling how flex and grid items are positioned along a container's main axis.
- [justify-items](references/flexbox-and-grid/justify-items.md) — Utilities for controlling how grid items are aligned along their inline axis.
- [justify-self](references/flexbox-and-grid/justify-self.md) — Utilities for controlling how an individual grid item is aligned along its inline axis.
- [align-content](references/flexbox-and-grid/align-content.md) — Utilities for controlling how rows are positioned in multi-row flex and grid containers.
- [align-items](references/flexbox-and-grid/align-items.md) — Utilities for controlling how flex and grid items are positioned along a container's cross axis.
- [align-self](references/flexbox-and-grid/align-self.md) — Utilities for controlling how an individual flex or grid item is positioned along its container's cross axis.
- [place-content](references/flexbox-and-grid/place-content.md) — Utilities for controlling how content is justified and aligned at the same time.
- [place-items](references/flexbox-and-grid/place-items.md) — Utilities for controlling how items are justified and aligned at the same time.
- [place-self](references/flexbox-and-grid/place-self.md) — Utilities for controlling how an individual item is justified and aligned at the same time.

### Spacing

- [padding](references/spacing/padding.md) — Utilities for controlling an element's padding.
- [margin](references/spacing/margin.md) — Utilities for controlling an element's margin.

### Sizing

- [width](references/sizing/width.md) — Utilities for setting the width of an element.
- [min-width](references/sizing/min-width.md) — Utilities for setting the minimum width of an element.
- [max-width](references/sizing/max-width.md) — Utilities for setting the maximum width of an element.
- [height](references/sizing/height.md) — Utilities for setting the height of an element.
- [min-height](references/sizing/min-height.md) — Utilities for setting the minimum height of an element.
- [max-height](references/sizing/max-height.md) — Utilities for setting the maximum height of an element.
- [inline-size](references/sizing/inline-size.md) — Utilities for setting the inline size of an element.
- [min-inline-size](references/sizing/min-inline-size.md) — Utilities for setting the minimum inline size of an element.
- [max-inline-size](references/sizing/max-inline-size.md) — Utilities for setting the maximum inline size of an element.
- [block-size](references/sizing/block-size.md) — Utilities for setting the block size of an element.
- [min-block-size](references/sizing/min-block-size.md) — Utilities for setting the minimum block size of an element.
- [max-block-size](references/sizing/max-block-size.md) — Utilities for setting the maximum block size of an element.

### Typography

- [font-family](references/typography/font-family.md) — Utilities for controlling the font family of an element.
- [font-size](references/typography/font-size.md) — Utilities for controlling the font size of an element.
- [font-smoothing](references/typography/font-smoothing.md) — Utilities for controlling the font smoothing of an element.
- [font-style](references/typography/font-style.md) — Utilities for controlling the style of text.
- [font-weight](references/typography/font-weight.md) — Utilities for controlling the font weight of an element.
- [font-stretch](references/typography/font-stretch.md) — Utilities for selecting the width of a font face.
- [font-variant-numeric](references/typography/font-variant-numeric.md) — Utilities for controlling the variant of numbers.
- [font-feature-settings](references/typography/font-feature-settings.md) — Utilities for controlling advanced typographic features.
- [letter-spacing](references/typography/letter-spacing.md) — Utilities for controlling the tracking, or letter spacing, of an element.
- [line-clamp](references/typography/line-clamp.md) — Utilities for clamping text to a specific number of lines.
- [line-height](references/typography/line-height.md) — Utilities for controlling the leading, or line height, of an element.
- [list-style-image](references/typography/list-style-image.md) — Utilities for controlling the marker images for list items.
- [list-style-position](references/typography/list-style-position.md) — Utilities for controlling the position of bullets and numbers in lists.
- [list-style-type](references/typography/list-style-type.md) — Utilities for controlling the marker style of a list.
- [text-align](references/typography/text-align.md) — Utilities for controlling the alignment of text.
- [color](references/typography/color.md) — Utilities for controlling the text color of an element.
- [text-decoration-line](references/typography/text-decoration-line.md) — Utilities for controlling the decoration of text.
- [text-decoration-color](references/typography/text-decoration-color.md) — Utilities for controlling the color of text decorations.
- [text-decoration-style](references/typography/text-decoration-style.md) — Utilities for controlling the style of text decorations.
- [text-decoration-thickness](references/typography/text-decoration-thickness.md) — Utilities for controlling the thickness of text decorations.
- [text-underline-offset](references/typography/text-underline-offset.md) — Utilities for controlling the offset of a text underline.
- [text-transform](references/typography/text-transform.md) — Utilities for controlling the capitalization of text.
- [text-overflow](references/typography/text-overflow.md) — Utilities for controlling how the text of an element overflows.
- [text-wrap](references/typography/text-wrap.md) — Utilities for controlling how text wraps within an element.
- [text-indent](references/typography/text-indent.md) — Utilities for controlling the amount of empty space shown before text in a block.
- [tab-size](references/typography/tab-size.md) — Utilities for controlling the size of tab characters.
- [vertical-align](references/typography/vertical-align.md) — Utilities for controlling the vertical alignment of an inline or table-cell box.
- [white-space](references/typography/white-space.md) — Utilities for controlling an element's white-space property.
- [word-break](references/typography/word-break.md) — Utilities for controlling word breaks in an element.
- [overflow-wrap](references/typography/overflow-wrap.md) — Utilities for controlling line breaks within words in an overflowing element.
- [hyphens](references/typography/hyphens.md) — Utilities for controlling how words should be hyphenated.
- [content](references/typography/content.md) — Utilities for controlling the content of the before and after pseudo-elements.

### Backgrounds

- [background-attachment](references/backgrounds/background-attachment.md) — Utilities for controlling how a background image behaves when scrolling.
- [background-clip](references/backgrounds/background-clip.md) — Utilities for controlling the bounding box of an element's background.
- [background-color](references/backgrounds/background-color.md) — Utilities for controlling an element's background color.
- [background-image](references/backgrounds/background-image.md) — Utilities for controlling an element's background image.
- [background-origin](references/backgrounds/background-origin.md) — Utilities for controlling how an element's background is positioned relative to borders, padding, and content.
- [background-position](references/backgrounds/background-position.md) — Utilities for controlling the position of an element's background image.
- [background-repeat](references/backgrounds/background-repeat.md) — Utilities for controlling the repetition of an element's background image.
- [background-size](references/backgrounds/background-size.md) — Utilities for controlling the background size of an element's background image.

### Borders

- [border-radius](references/borders/border-radius.md) — Utilities for controlling the border radius of an element.
- [border-width](references/borders/border-width.md) — Utilities for controlling the width of an element's borders.
- [border-color](references/borders/border-color.md) — Utilities for controlling the color of an element's borders.
- [border-style](references/borders/border-style.md) — Utilities for controlling the style of an element's borders.
- [outline-width](references/borders/outline-width.md) — Utilities for controlling the width of an element's outline.
- [outline-color](references/borders/outline-color.md) — Utilities for controlling the color of an element's outline.
- [outline-style](references/borders/outline-style.md) — Utilities for controlling the style of an element's outline.
- [outline-offset](references/borders/outline-offset.md) — Utilities for controlling the offset of an element's outline.

### Effects

- [box-shadow](references/effects/box-shadow.md) — Utilities for controlling the box shadow of an element.
- [text-shadow](references/effects/text-shadow.md) — Utilities for controlling the shadow of a text element.
- [opacity](references/effects/opacity.md) — Utilities for controlling the opacity of an element.
- [mix-blend-mode](references/effects/mix-blend-mode.md) — Utilities for controlling how an element should blend with the background.
- [background-blend-mode](references/effects/background-blend-mode.md) — Utilities for controlling how an element's background image should blend with its background color.
- [mask-clip](references/effects/mask-clip.md) — Utilities for controlling the bounding box of an element's mask.
- [mask-composite](references/effects/mask-composite.md) — Utilities for controlling how multiple masks are combined together.
- [mask-image](references/effects/mask-image.md) — Utilities for controlling an element's mask image.
- [mask-mode](references/effects/mask-mode.md) — Utilities for controlling an element's mask mode.
- [mask-origin](references/effects/mask-origin.md) — Utilities for controlling how an element's mask image is positioned relative to borders, padding, and content.
- [mask-position](references/effects/mask-position.md) — Utilities for controlling the position of an element's mask image.
- [mask-repeat](references/effects/mask-repeat.md) — Utilities for controlling the repetition of an element's mask image.
- [mask-size](references/effects/mask-size.md) — Utilities for controlling the size of an element's mask image.
- [mask-type](references/effects/mask-type.md) — Utilities for controlling how an SVG mask is interpreted.

### Filters

- [blur](references/filters/filter-blur.md) — Utilities for applying blur filters to an element.
- [brightness](references/filters/filter-brightness.md) — Utilities for applying brightness filters to an element.
- [contrast](references/filters/filter-contrast.md) — Utilities for applying contrast filters to an element.
- [drop-shadow](references/filters/filter-drop-shadow.md) — Utilities for applying drop-shadow filters to an element.
- [grayscale](references/filters/filter-grayscale.md) — Utilities for applying grayscale filters to an element.
- [hue-rotate](references/filters/filter-hue-rotate.md) — Utilities for applying hue-rotate filters to an element.
- [invert](references/filters/filter-invert.md) — Utilities for applying invert filters to an element.
- [saturate](references/filters/filter-saturate.md) — Utilities for applying saturation filters to an element.
- [sepia](references/filters/filter-sepia.md) — Utilities for applying sepia filters to an element.
- [blur](references/filters/backdrop-filter-blur.md) — Utilities for applying backdrop blur filters to an element.
- [brightness](references/filters/backdrop-filter-brightness.md) — Utilities for applying backdrop brightness filters to an element.
- [contrast](references/filters/backdrop-filter-contrast.md) — Utilities for applying backdrop contrast filters to an element.
- [grayscale](references/filters/backdrop-filter-grayscale.md) — Utilities for applying backdrop grayscale filters to an element.
- [hue-rotate](references/filters/backdrop-filter-hue-rotate.md) — Utilities for applying backdrop hue-rotate filters to an element.
- [invert](references/filters/backdrop-filter-invert.md) — Utilities for applying backdrop invert filters to an element.
- [opacity](references/filters/backdrop-filter-opacity.md) — Utilities for applying backdrop opacity filters to an element.
- [saturate](references/filters/backdrop-filter-saturate.md) — Utilities for applying backdrop saturation filters to an element.
- [sepia](references/filters/backdrop-filter-sepia.md) — Utilities for applying backdrop sepia filters to an element.

### Tables

- [border-collapse](references/tables/border-collapse.md) — Utilities for controlling whether table borders should collapse or be separated.
- [border-spacing](references/tables/border-spacing.md) — Utilities for controlling the spacing between table borders.
- [table-layout](references/tables/table-layout.md) — Utilities for controlling the table layout algorithm.
- [caption-side](references/tables/caption-side.md) — Utilities for controlling the alignment of a caption element inside of a table.

### Transitions & Animation

- [transition-property](references/transitions-and-animation/transition-property.md) — Utilities for controlling which CSS properties transition.
- [transition-behavior](references/transitions-and-animation/transition-behavior.md) — Utilities to control the behavior of CSS transitions.
- [transition-duration](references/transitions-and-animation/transition-duration.md) — Utilities for controlling the duration of CSS transitions.
- [transition-timing-function](references/transitions-and-animation/transition-timing-function.md) — Utilities for controlling the easing of CSS transitions.
- [transition-delay](references/transitions-and-animation/transition-delay.md) — Utilities for controlling the delay of CSS transitions.
- [animation](references/transitions-and-animation/animation.md) — Utilities for animating elements with CSS animations.

### Transforms

- [backface-visibility](references/transforms/backface-visibility.md) — Utilities for controlling if an element's backface is visible.
- [perspective](references/transforms/perspective.md) — Utilities for controlling an element's perspective when placed in 3D space.
- [perspective-origin](references/transforms/perspective-origin.md) — Utilities for controlling an element's perspective origin when placed in 3D space.
- [rotate](references/transforms/rotate.md) — Utilities for rotating elements.
- [scale](references/transforms/scale.md) — Utilities for scaling elements.
- [skew](references/transforms/skew.md) — Utilities for skewing elements with transform.
- [transform](references/transforms/transform.md) — Utilities for transforming elements.
- [transform-origin](references/transforms/transform-origin.md) — Utilities for specifying the origin for an element's transformations.
- [transform-style](references/transforms/transform-style.md) — Utilities for controlling if an elements children are placed in 3D space.
- [translate](references/transforms/translate.md) — Utilities for translating elements.
- [zoom](references/transforms/zoom.md) — Utilities for scaling elements using zoom.

### Interactivity

- [accent-color](references/interactivity/accent-color.md) — Utilities for controlling the accented color of a form control.
- [appearance](references/interactivity/appearance.md) — Utilities for suppressing native form control styling.
- [caret-color](references/interactivity/caret-color.md) — Utilities for controlling the color of the text input cursor.
- [color-scheme](references/interactivity/color-scheme.md) — Utilities for controlling the color scheme of an element.
- [cursor](references/interactivity/cursor.md) — Utilities for controlling the cursor style when hovering over an element.
- [field-sizing](references/interactivity/field-sizing.md) — Utilities for controlling the sizing of form controls.
- [pointer-events](references/interactivity/pointer-events.md) — Utilities for controlling whether an element responds to pointer events.
- [resize](references/interactivity/resize.md) — Utilities for controlling how an element can be resized.
- [scroll-behavior](references/interactivity/scroll-behavior.md) — Utilities for controlling the scroll behavior of an element.
- [scrollbar-color](references/interactivity/scrollbar-color.md) — Utilities for controlling the color of an element's scrollbar.
- [scrollbar-width](references/interactivity/scrollbar-width.md) — Utilities for controlling the width of an element's scrollbar.
- [scrollbar-gutter](references/interactivity/scrollbar-gutter.md) — Utilities for controlling the gutter space reserved for an element's scrollbar.
- [scroll-margin](references/interactivity/scroll-margin.md) — Utilities for controlling the scroll offset around items in a snap container.
- [scroll-padding](references/interactivity/scroll-padding.md) — Utilities for controlling an element's scroll offset within a snap container.
- [scroll-snap-align](references/interactivity/scroll-snap-align.md) — Utilities for controlling the scroll snap alignment of an element.
- [scroll-snap-stop](references/interactivity/scroll-snap-stop.md) — Utilities for controlling whether you can skip past possible snap positions.
- [scroll-snap-type](references/interactivity/scroll-snap-type.md) — Utilities for controlling how strictly snap points are enforced in a snap container.
- [touch-action](references/interactivity/touch-action.md) — Utilities for controlling how an element can be scrolled and zoomed on touchscreens.
- [user-select](references/interactivity/user-select.md) — Utilities for controlling whether the user can select text in an element.
- [will-change](references/interactivity/will-change.md) — Utilities for optimizing upcoming animations of elements that are expected to change.

### SVG

- [fill](references/svg/fill.md) — Utilities for styling the fill of SVG elements.
- [stroke](references/svg/stroke.md) — Utilities for styling the stroke of SVG elements.
- [stroke-width](references/svg/stroke-width.md) — Utilities for styling the stroke width of SVG elements.

### Accessibility

- [forced-color-adjust](references/accessibility/forced-color-adjust.md) — Utilities for opting in and out of forced colors.
