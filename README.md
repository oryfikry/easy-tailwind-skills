# tailwindcss-docs

Offline copy of the Tailwind CSS v4 documentation, split into one markdown file per page so an AI agent can read only what it needs.

- Source: official docs repo, [tailwindlabs/tailwindcss.com](https://github.com/tailwindlabs/tailwindcss.com) (`main`), fetched 2026-09-30.
- Content belongs to Tailwind Labs. This folder is a converted copy for local reference.
- 220 files, about 2.2 MB.

## Use it

Point an agent at the entry file:

```
<path-to>/tailwindcss-docs/SKILL.md
```

`SKILL.md` lists every page with a one-line description. The agent picks a page from the index and opens only that file.

To load it automatically as a Claude Code skill, put the folder in `~/.claude/skills/` (all projects) or `<project>/.claude/skills/` (one project). Claude then uses it when a task involves Tailwind. Links between pages are relative, so the folder works from any location.

## Layout

```
tailwindcss-docs/
├── SKILL.md            entry point: usage rules + index of all pages
├── README.md           this file
└── references/
    ├── getting-started/     installation overview, editor setup, compatibility, upgrade guide
    ├── installation/        Vite, PostCSS, CLI, CDN + framework-guides/ (19 frameworks)
    ├── core-concepts/       utility classes, variants, responsive, dark mode, theme, colors,
    │                        custom styles, functions and directives, default-theme.css
    ├── base-styles/         preflight
    └── layout, flexbox-and-grid, spacing, sizing, typography, backgrounds, borders,
        effects, filters, tables, transitions-and-animation, transforms,
        interactivity, svg, accessibility     one file per utility
```

## Reading a page

- A utility page starts with a class → CSS table, then examples, then "Using a custom value", "Responsive design" and "Customizing your theme" sections.
- `**name**` above a code block is its filename or tab label.
- A `diff` block marks lines the docs show as removed (`-`) and added (`+`).
- `references/core-concepts/default-theme.css` is the full default theme: fonts, colors, spacing, breakpoints, shadows, easings.

## What differs from the website

- Rendered demos, screenshots and hidden decorative SVGs are removed. Every code sample is kept.
- The default color palette is regenerated as a table in `colors.md`, since the site draws it with a React component.
- Boilerplate sections that the site builds from shared templates are expanded into plain markdown.
- Installation and framework guides keep their steps and code, not the site's extra intro text.
- One upstream page, `justify-items`, has an unclosed tag in its source. Its content is intact.

## Keeping it current

These files are generated from the docs source, so do not edit them by hand. Edits are lost on the next refresh. To update, re-run the conversion against the latest `main` and replace the `references/` folder and `SKILL.md`. The `Source:` line at the top of each page links to the live page for comparison.
