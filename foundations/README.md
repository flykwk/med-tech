# Foundations

The foundations are the lowest layer of the design system: small sets of named, reusable decisions that components and patterns are built from.

**System name:** [Name] · **Version:** [1.0] · **Owner:** [Name / team] · **Last updated:** [Date]

| Foundation | What it defines |
|---|---|
| [Principles](./principles.md) | How design decisions are made and settled |
| [Design tokens](./tokens.md) | Naming convention and the primitive, semantic and component tiers |
| [Color](./color.md) | Brand colors, feedback colors and contrast rules |
| [Typography](./typography.md) | Typefaces, type scale and text rules |
| [Spacing and layout](./spacing-layout.md) | Spacing scale, grid, breakpoints and touch targets |
| [Elevation and shape](./elevation-shape.md) | Shadow levels, radii and borders |
| [Iconography](./iconography.md) | Icon style, sizing and imagery rules |
| [Motion](./motion.md) | Durations, easing and reduced-motion support |
| [Accessibility](./accessibility.md) | WCAG targets, keyboard, focus and semantics |
| [Content and voice](./content-voice.md) | Tone, UI text and formats |

Governance (how to propose, review and release changes) lives in [CONTRIBUTING.md](../CONTRIBUTING.md).

## How the layers fit together

Foundations and tokens, then components (buttons, inputs), then patterns (forms, navigation), then templates and pages.

## Core rules that apply everywhere

1. Use tokens, never raw values.
2. Every value is defined once and referenced everywhere else.
3. Choose from the scale; do not invent new values without a documented request.
4. Accessibility is a requirement, not an enhancement.
5. If a foundation does not cover a need, propose an addition rather than a workaround.
