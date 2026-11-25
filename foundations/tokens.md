# Design Tokens

## Purpose

Design tokens store foundation decisions as named values so there is a single source of truth. Components reference the token, so changing it updates everything that uses it. Tokens also carry the theme mode, so one component can render correctly in both light and dark themes.

## Naming convention

| Tier | Pattern | Examples |
|---|---|---|
| Primitive | `[hue]-[mode]-[step]` | `red-light-500`, `red-dark-500`, `green-light-50` |
| Semantic | `[category]-[property]-[variant]-[role]` | `color-feedback-error-surface`, `color-feedback-success-text` |
| Component | `[component]-[variant]-[property]` | `alert-error-bg` |

- **Hue** is the palette name, for example `red`, `amber`, `green`.
- **Mode** is `light` or `dark`. It appears in primitive names only.
- **Step** is `50, 100, 200, 300, 400, 500, 600, 700, 800, 900`.

Semantic and component tokens have no mode in their name. The active theme decides which primitive they resolve to.

## Token tiers

| Tier | Purpose | Example |
|---|---|---|
| Primitive (global) | Raw values, one set per mode. Never used directly in components | `red-light-50: #FFF0F2`, `red-dark-50: #250909` |
| Semantic (alias) | Meaning-based. References a primitive and resolves per mode | `color-feedback-error-surface: {red-light-50}` in light, `{red-dark-50}` in dark |
| Component | Scoped to one component | `alert-error-bg: {color-feedback-error-surface}` |

## Theme modes

The system supports two modes: **light** and **dark**.

- Each hue has a light scale and a dark scale with the same ten steps.
- A dark step keeps the role of the light step with the same number, so a semantic token points to the same step number in both modes.

| Steps | Role in both modes |
|---|---|
| 50 to 200 | Surfaces, tints and borders |
| 300 to 600 | Decorative fills. Not for text or required graphics |
| 700 | Solid: icons, indicators and fills behind on-solid text |
| 800 to 900 | Text |

- Light scales run from light (50) to dark (900). Dark scales run from dark (50) to light (900).
- In Figma, store each semantic token as one variable with a **Light** and a **Dark** mode. In code, publish the same tokens as CSS custom properties switched by a theme attribute.

## Rules

- Components may only reference semantic or component tokens.
- Never reference a mode-specific primitive (`*-light-*` or `*-dark-*`) in a component; use a semantic token so theme switching needs no component changes.
- Do not put the mode in semantic or component token names.
- Every semantic token must have a value for both light and dark before it is published.
- Every pairing a semantic token creates must meet WCAG 2.2 AA in both modes before it is published: 4.5:1 for text, 3:1 for meaningful icons and indicators. Record the ratios in [color](./color.md#contrast-check).
- Tokens are stored in [Figma Variables / JSON / Style Dictionary] as the single source of truth.
- Deprecated tokens are kept for [N] releases with a replacement noted.

## Token file

<!-- Link to /tokens/tokens.json if you add one. -->

[Back to foundations](./README.md)
