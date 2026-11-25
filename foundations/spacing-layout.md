# Spacing and Layout

## Purpose

[How spacing and layout create rhythm, grouping and consistency.]

## Base unit

[4px / 8px]

## Spacing scale

| Token | Value | Typical use |
|---|---|---|
| `space-xs` | [4px] | [Icon to label] |
| `space-sm` | [8px] | [Related elements] |
| `space-md` | [16px] | [Default padding] |
| `space-lg` | [24px] | [Between groups] |
| `space-xl` | [32px] | [Between sections] |
| `space-2xl` | [48px] | [Page-level separation] |

## Grid and breakpoints

| Breakpoint | Min width | Columns | Gutter | Margin |
|---|---|---|---|---|
| Mobile | [0] | [4] | [16] | [16] |
| Tablet | [768] | [8] | [24] | [32] |
| Desktop | [1200] | [12] | [24] | [auto] |

## Rules

- All spacing uses scale tokens; no arbitrary pixel values.
- Closer spacing means closer relationship (proximity groups related items).
- Minimum touch target: [44 x 44px] (or [24 x 24px] with spacing on desktop pointer UIs).

## Do and don't

<!-- Add layout examples. -->

[Back to foundations](./README.md)
