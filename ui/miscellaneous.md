# UI notes

Conventions of the Lexicora interface that are not in the theme file. The tokens themselves are in [`shadcn-theme.css`](shadcn-theme.css).

## Stack

[Tailwind CSS v4](https://tailwindcss.com) with [shadcn/ui](https://ui.shadcn.com). Dark mode is a `.dark` class on `<html>`:

```css
@custom-variant dark (&:is(.dark *));
```

## Radius

`--radius: 0.625rem`. The `sm`, `md`, `lg` and `xl` radii derive from it (`-4px`, `-2px`, `+0`, `+4px`).

## Logo in light and dark

Two helper classes show one logo or the other with no JavaScript:

```css
.lc-display-light,
.dark .lc-display-dark { display: block; }
.lc-display-dark,
.dark .lc-display-light { display: none; }
```

An inline SVG can instead take its fill from `--lc-logo-foreground`, which is navy in light mode and white in dark.

## Scrollbars

Thin scrollbars, with a transparent track.

| | Thumb | Thumb on hover |
| --- | --- | --- |
| Light | `#adadad` | `#5e5f61` |
| Dark | `#50565d` (Firefox: `#4d5359`) | `#868b8f` |

`.scrollbar-bg-transparent` is for scrollable areas inside cards (`#b2b2b2` light, `#535961` dark). The page's `--lc-scrollbar-offset` keeps content from shifting when a scrollbar appears.

## Selection and spelling

- Text selection: `#2383e247`
- Spelling and grammar errors: a dotted 2px underline, offset 2px, with no ink skipping

## Focus

Focus rings show only while navigating by keyboard, and always in text fields (where the caret has to be found). The extension sets a `data-input-modality="keyboard"` attribute on the root and overrides Tailwind's `focus-visible` variant to follow it.

## Motion

- Default view transition: 0.15 s.
- `.animate-icon-pop`: a 0.3 s settle from scale 1.1 through 0.92 to 1, with `cubic-bezier(0.175, 0.885, 0.32, 1.275)`.
- `prefers-reduced-motion` turns off smooth scrolling.
- `.lc-no-transitions` switches off every transition and animation inside an element.

## Bottom bar blur

`.lc-bottom-bar-styled-bg` fades content out under a bar fixed to the bottom, with an inset shadow in the background color and a masked 6px backdrop blur. The shadow is stronger in dark mode.
