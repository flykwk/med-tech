# Design Tokens

## Purpose

Design tokens store foundation decisions as named values so there is a single source of truth. Components reference the token, so changing it updates everything that uses it. Tokens also carry the theme mode, so one component can render correctly in both light and dark themes.

## Naming convention

| Tier | Pattern | Examples |
|---|---|---|
| Primitive | `[hue]-[mode]-[step]` | `red-light-500`, `red-dark-500`, `green-light-50` |
| Semantic | `[category]-[property]-[variant]-[role]` | `color-feedback-error-surface`, `color-feedback-success-text`, `color-brand-primary-solid` |
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

In Figma each tier is its own collection: **Primitives**, **Semantic** (Light and Dark modes) and **Component**. The Component collection has a single mode because it only aliases semantic tokens, which already switch with the theme.

## Theme modes

The system supports two modes: **light** and **dark**.

- Each hue has a light scale and a dark scale with the same ten steps.
- A dark step keeps the role of the light step with the same number, so a semantic token points to the same step number in both modes. The one exception is the neutral surface tokens, whose light and dark steps differ (see [UI hierarchy](./color.md#ui-hierarchy)).

| Steps | Role in both modes |
|---|---|
| 50 to 200 | Surfaces, tints and borders |
| 300 to 600 | Decorative fills. Not for text or required graphics |
| 700 | Solid: icons, indicators and fills behind on-solid text |
| 800 to 900 | Text |

- Light scales run from light (50) to dark (900). Dark scales run from dark (50) to light (900).
- In Figma, store each semantic token as one variable with a **Light** and a **Dark** mode. In code, publish the same tokens as CSS custom properties switched by a theme attribute.

## Mode dimensions

A mode dimension is one way a value can change without changing its meaning. Each dimension lives in its own Figma collection with its own modes, so dimensions combine without multiplying variables: three themes, three surface levels and three densities are three small collections, not 27 sets of tokens.

| Dimension | Modes | Collection | Status | What it changes |
|---|---|---|---|---|
| Theme | Light, Dark | Semantic | In use | All color tokens |
| Surface level | Canvas, Card, Table | Surface level | Reserved | Colors that must differ from their parent surface: subtle border, hover fill, input background |
| Density | Compact, Default, Comfortable | Density | Reserved | Padding, gaps and row heights |
| Breakpoint | Desktop, Tablet | Breakpoint | Reserved | Text sizes and layout spacing |

Rules for adding a dimension:

- Add a dimension only when a component needs it. A reserved dimension is not built until then.
- Keep number primitives mode-free, for example `space-8` and `font-size-14`. A dimension changes which primitive a semantic token points to.
- Name semantic tokens for their role, not their size: `space-inset-card` and `text-size-body`, not `space-16` and `text-size-14`. The role name keeps working when a mode is added later.
- Surface level applies only to tokens that depend on their parent. Text, icon and strong-border tokens already pass AA on all three surfaces with one value, so they stay outside it.
- Verify every mode combination before publishing, for example each theme on each surface level.
- Every dimension needs a matching mechanism in code, such as `data-theme`, `data-surface` and `data-density` attributes that override the CSS custom properties.
- A device may allow only one density or breakpoint, for example where touch-target size or legibility is a usability requirement.
- Check the mode limit of the Figma plan before planning a dimension with many modes.

## Rules

- Components may only reference semantic or component tokens.
- Never reference a mode-specific primitive (`*-light-*` or `*-dark-*`) in a component; use a semantic token so theme switching needs no component changes.
- Do not put the mode in semantic or component token names.
- Every semantic token must have a value for both light and dark before it is published.
- Every pairing a semantic token creates must meet WCAG 2.2 AA in both modes before it is published: 4.5:1 for text, 3:1 for meaningful icons and indicators. Record the ratios in the contrast check tables in [color](./color.md).
- Tokens are stored in [Figma Variables / JSON / Style Dictionary] as the single source of truth.
- Deprecated tokens are kept for [N] releases with a replacement noted.

## Token file

<!-- Link to /tokens/tokens.json if you add one. -->

[Back to foundations](./README.md)
