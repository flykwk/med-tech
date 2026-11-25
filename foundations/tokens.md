# Design Tokens

## Purpose

Design tokens store foundation decisions as named values so there is a single source of truth. Components reference the token, so changing it updates everything that uses it.

## Naming convention

`[category]-[property]-[variant]-[state]`

Examples: `color-background-surface-default`, `space-inline-md`, `text-heading-lg`

## Token tiers

| Tier | Purpose | Example |
|---|---|---|
| Primitive (global) | Raw values, never used directly in components | `blue-600: [#0057B8]` |
| Semantic (alias) | Meaning-based, references a primitive | `color-action-primary: {blue-600}` |
| Component | Scoped to one component | `button-primary-bg: {color-action-primary}` |

## Rules

- Components may only reference semantic or component tokens.
- Tokens are stored in [Figma Variables / JSON / Style Dictionary] as the single source of truth.
- Deprecated tokens are kept for [N] releases with a replacement noted.

## Token file

<!-- Link to /tokens/tokens.json if you add one. -->

[Back to foundations](./README.md)
