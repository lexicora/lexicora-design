# Color palette

All values are taken from the Lexicora extension's theme. The ready-to-use CSS is in [`ui/shadcn-theme.css`](../ui/shadcn-theme.css). Colors are written in `oklch()`, the grays are the Tailwind CSS v4 cool-gray scale, nudged where noted.

## Brand

| Role | Value | Used for |
| --- | --- | --- |
| Lexicora navy | `#00143d` | The logo mark, and the logo on light backgrounds |
| White | `#ffffff` | The logo mark on dark backgrounds, and the logo tile |

In the UI the navy is exposed as `--lc-logo-foreground`: `#00143d` in light mode, `#ffffff` in dark mode, so an inline SVG logo follows the theme.

## Light theme

| Token | Value | Notes |
| --- | --- | --- |
| `--background` | `oklch(0.955 0.004 264.5)` | Slightly above the gray-100/200 midpoint |
| `--foreground` | `oklch(0.13 0.028 261.692)` | |
| `--card` | `oklch(1 0 0)` | |
| `--card-hover` | `oklch(0.915 0.007 263)` | Between gray-200 and gray-300 |
| `--input-bg` | `oklch(0.985 0.002 247.839)` | gray-50: inputs sit between background and card |
| `--primary` | `oklch(0.21 0.034 264.665)` | |
| `--primary-foreground` | `oklch(0.985 0.002 247.839)` | |
| `--secondary`, `--muted`, `--accent` | `oklch(0.883 0.009 260)` | gray-200, shifted to match the background |
| `--muted-foreground` | `oklch(0.551 0.027 264.364)` | |
| `--border`, `--input` | `oklch(0.872 0.01 258.338)` | gray-300 |
| `--ring` | `oklch(0.707 0.022 261.325)` | |
| `--destructive` | `oklch(0.577 0.245 27.325)` | |

## Dark theme

| Token | Value | Notes |
| --- | --- | --- |
| `--background` | `oklch(0.13 0.028 261.692)` | |
| `--foreground` | `oklch(0.985 0.002 247.839)` | |
| `--card`, `--popover` | `oklch(0.21 0.034 264.665)` | |
| `--card-hover` | `oklch(0.29 0.033 257)` | Lighter than the card, for a visible hover lift |
| `--primary` | `oklch(0.928 0.006 264.531)` | |
| `--primary-foreground` | `oklch(0.21 0.034 264.665)` | |
| `--secondary`, `--muted`, `--accent` | `oklch(0.278 0.033 256.848)` | |
| `--muted-foreground` | `oklch(0.707 0.022 261.325)` | |
| `--border` | `oklch(1 0 0 / 10%)` | |
| `--input` | `oklch(1 0 0 / 15%)` | |
| `--ring` | `oklch(0.551 0.027 264.364)` | |
| `--destructive` | `oklch(0.704 0.191 22.216)` | |

## Lexicora-specific tokens

| Token | Light | Dark | Used for |
| --- | --- | --- | --- |
| `--lc-muted-foreground` | `oklch(0.36 0.027 264.364)` | `oklch(0.81 0.022 261.325)` | Secondary text that must stay readable |
| `--lc-muted-foreground-hover` | `oklch(0.34 0.027 263)` | `oklch(0.84 0.015 255)` | Its hover state |
| `--lc-text-color-monospace` | `oklch(50.153% 0.19988 28.587)` | `oklch(65.34% 0.183 23.68)` | Inline code text |
| `--lc-light-foreground-color` | `oklch(0.985 0.002 247.839)` | same | Text on dark surfaces in either theme |
| `--lc-logo-foreground` | `#00143d` | `#ffffff` | The logo |

## Charts

`--chart-1` to `--chart-5` are the shadcn chart colors, one set per theme; see `ui/shadcn-theme.css`.

## Light and dark

Both themes are first-class. The theme is a `.light` or `.dark` class on `<html>`, set before the first paint so a page never opens in the wrong colors, and Tailwind's `dark:` variant follows the `.dark` class.
