# Typography

Lexicora uses two typefaces, both open source and both available as variable fonts through [Fontsource](https://fontsource.org).

| Role | Typeface | License | npm package |
| --- | --- | --- | --- |
| Interface and body text | [Wix Madefor Text](https://fonts.google.com/specimen/Wix+Madefor+Text) | OFL-1.1 | `@fontsource-variable/wix-madefor-text` |
| Code and monospace | [JetBrains Mono](https://www.jetbrains.com/lp/mono/) | OFL-1.1 | `@fontsource-variable/jetbrains-mono` |

The fonts are third-party and keep their own licenses; this repository does not redistribute them.

## Font stacks

```css
--lc-font-sans:
  "Wix Madefor Text Variable", system-ui, "Segoe UI", -apple-system, Avenir,
  Helvetica, Arial, sans-serif;
--lc-font-monospace:
  "JetBrains Mono Variable", ui-monospace, SFMono-Regular, Menlo, Monaco,
  Consolas, "Liberation Mono", "Courier New", monospace;
```

With Tailwind, both are available as `font-lc-sans` and `font-lc-monospace`.

## Loading

```ts
import "@fontsource-variable/wix-madefor-text/wght.css";
import "@fontsource-variable/wix-madefor-text/wght-italic.css";
import "@fontsource-variable/jetbrains-mono/wght.css";
```

## Base text

```css
body {
  font-family: var(--lc-font-sans);
  line-height: 1.5;
  font-weight: 400;
  font-size: 78%;
}
```

The base size is `78%`, not the browser default: Wix Madefor Text runs larger than Inter, and 78% makes it read at the same size as Inter at the usual 75%.

## Weights

Both fonts are variable, so every weight comes from one file per style. Body text is 400.

## Code

Inline code and code blocks use the monospace stack. Inline code text is colored with `--lc-text-color-monospace`, a red that has its own light and dark value (see [`color-palette.md`](color-palette.md)).
