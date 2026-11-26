# Color

## Purpose

Color in this system carries clinical status and hierarchy. The feedback palettes (red, amber, green) communicate risk and state, and each one has a light and a dark scale so interfaces stay legible in both themes.

<!-- Add a screenshot of your palettes here. -->

## Theme modes

Every palette is defined twice: `[hue]-light-[step]` and `[hue]-dark-[step]`. Steps keep the same role in both modes (see [tokens](./tokens.md#theme-modes)), so components use semantic tokens and never reference a mode directly.

| Steps | Role in both modes |
|---|---|
| 50 to 200 | Surfaces, tints and borders |
| 300 to 600 | Decorative fills. Not for text or required graphics |
| 700 | Solid: icons, indicators and fills behind on-solid text |
| 800 to 900 | Text |

## Brand and neutral palette

| Role | Token | Light value | Dark value | Usage |
|---|---|---|---|---|
| Brand primary | `color-brand-primary` | [#] | [#] | [Key actions, brand moments] |
| Brand secondary | `color-brand-secondary` | [#] | [#] | [Supporting accents] |
| Neutral scale | `neutral-[light/dark]-[50-900]` | [#] | [#] | [Text, borders, surfaces] |
| Info | `color-feedback-info` | [#] | [#] | [Neutral information] |

## Feedback palettes

### Red: error and critical

Namespace `clinical.vitals.red`. Reference standard: ISO 3864 / IEC 60601.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | `#FFF0F2` | `#210D0D` | Clinical Pink | Low Risk | Low-severity backgrounds, safe observation bounds |
| 100 | `#FFCCD3` | `#2F1314` | Clinical Rose | Mild Alert | Attention indicator, borderline diagnostic values |
| 200 | `#FFA2A2` | `#451E1F` | Medical Coral | Moderate | Moderate severity warnings, pending clinical review |
| 300 | `#FF3B30` | `#7E2F33` | Arterial Red | Arterial | Oxygenated blood flow, standard critical boundary |
| 400 | `#D12626` | `#B54249` | Venous Red | Venous | Deoxygenated blood, lab classification standards |
| 500 | `#E60000` | `#E45B63` | Critical Red | Critical | Immediate vitals warning, patient risk threshold |
| 600 | `#C20000` | `#F68486` | Emergency | Emergency | Life-critical failure states, system stop triggers |
| 700 | `#990000` | `#FEAAA9` | Biohazard Red | Biohazard | Active hazard zoning, infectious agent presence |
| 800 | `#6D000D` | `#FBD3D2` | Clinical Maroon | Deep Maroon | Secondary trend failures, pathology classification |
| 900 | `#2F0004` | `#FEE9E8` | Near-Black Red | Extreme Alert | Extreme clinical crisis, imminent danger status |

Token names: `red-light-50` to `red-light-900`, `red-dark-50` to `red-dark-900`.

### Amber: warning and caution

Governs caution indicators, pending triage queues, medium-risk vitals and non-fatal medication interaction flags. Tuned for optical comfort in low-light hospital environments.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | `#FFFDF2` | `#1C1202` | Amber 50 | Informational | Soft clinical cream for backgrounds |
| 100 | `#FEFCE8` | `#271A01` | Amber 100 | Low Caution | Light amber for low-caution alerts |
| 200 | `#FEF3C7` | `#3A2800` | Amber 200 | Mild Alert | Secondary attention, non-urgent states |
| 300 | `#FDE68A` | `#644701` | Amber 300 | Pending | Warm amber for pending status and tasks |
| 400 | `#FCD34D` | `#8E6704` | Amber 400 | Moderate Warning | Standard clinical amber for alerts |
| 500 | `#F59E0B` | `#B78500` | Amber 500 | Elevated Risk | Deep amber for active caution flags |
| 600 | `#D97706` | `#D6A12B` | Amber 600 | High Caution | Burnt amber for persistent risk status |
| 700 | `#B45309` | `#E5BE77` | Amber 700 | Urgent Review | Dark amber for immediate clinical checks |
| 800 | `#92400E` | `#EDDCBD` | Amber 800 | Severe Caution | Near-brown amber for critical delays |
| 900 | `#451A03` | `#F7EDDC` | Amber 900 | Severe Risk | Extreme dark amber warning threshold |

Token names: `amber-light-50` to `amber-light-900`, `amber-dark-50` to `amber-dark-900`.

### Green: success and pass

Specification: Standards v4.2. Used for healthy physiological signs, within-threshold lab results, verified authorization states and validated medical devices.

| Step | Light value | Dark value | Name | Example | Usage |
|---|---|---|---|---|---|
| 50 | `#F0FDF4` | `#07180B` | Normal BG | Patient Chart BG | Soft clinical mint for background states |
| 100 | `#DCFCE7` | `#0B2311` | In Range | Vitals Safe Zone | Light green for safe within-range highlights |
| 200 | `#BBF7D0` | `#11331B` | Healthy | Optimal BMI Stat | Spring green for optimal healthy indicators |
| 300 | `#86EFAC` | `#0B5D2A` | Pass | Lab Test Cleared | Standard clinical green for pass and cleared |
| 400 | `#4ADE80` | `#02853C` | Cleared | Discharge Approved | Medium green for verified normal ranges |
| 500 | `#22C55E` | `#1EAB53` | Verified | EHR Auth Confirmed | Deep green for confirmed safe parameters |
| 600 | `#16A34A` | `#62C37A` | Approved | Device Connected | Forest green for strong verified states |
| 700 | `#15803D` | `#95D7A2` | Confirmed | Identity Matched | Dark green for absolute clinical cleared |
| 800 | `#166534` | `#CAE7CF` | Safe | Critical Safe Alert | Deep forest for high-contrast safety text |
| 900 | `#14532D` | `#E3F4E6` | Absolute | Final Sign-off | Near-black green for absolute verification |

Token names: `green-light-50` to `green-light-900`, `green-dark-50` to `green-dark-900`.

## Semantic mapping by mode

| Semantic token | Light mode | Dark mode | Usage |
|---|---|---|---|
| `color-feedback-[role]-surface` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Tinted background of an alert or status container |
| `color-feedback-[role]-border` | `{[hue]-light-200}` | `{[hue]-dark-200}` | Decorative divider. A control that relies on its border alone must use the solid token |
| `color-feedback-[role]-solid` | `{[hue]-light-700}` | `{[hue]-dark-700}` | Status icons and indicators (3:1 or more against the surface) |
| `color-feedback-[role]-on-solid` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Text and icons placed on the solid color |
| `color-feedback-[role]-text` | `{[hue]-light-800}` | `{[hue]-dark-800}` | Text on the surface, subtle surface and hover surface |

Roles and hues: `error` uses `red`, `warning` uses `amber`, `success` uses `green`. For example, `color-feedback-error-text` is `{red-light-800}` in light mode and `{red-dark-800}` in dark mode.

## Contrast check

WCAG 2.2 AA ratios for every pairing the semantic tokens create, calculated from the hex values above. Text needs 4.5:1. Meaningful icons and indicators need 3:1.

| Pairing | Requirement | Red light | Red dark | Amber light | Amber dark | Green light | Green dark |
|---|---|---|---|---|---|---|---|
| Text (800) on surface (50) | 4.5:1 | 11.47 | 13.61 | 6.95 | 13.70 | 6.81 | 13.84 |
| Text (800) on subtle surface (100) | 4.5:1 | 8.95 | 12.54 | 6.85 | 12.62 | 6.49 | 12.55 |
| Text (800) on hover surface (200) | 4.5:1 | 6.61 | 10.52 | 6.37 | 10.50 | 5.88 | 10.47 |
| Solid (700) on surface (50) | 3:1 | 8.07 | 10.23 | 4.92 | 10.52 | 4.79 | 10.94 |
| On-solid (50) on solid (700) | 4.5:1 | 8.07 | 10.23 | 4.92 | 10.52 | 4.79 | 10.94 |

All pairings pass in both modes.

Steps 300 to 600 are decorative. They are not guaranteed to meet 3:1 or 4.5:1 against the surface, so never use them for text or as the only way to show status. For example, `amber-light-500` is 2.11:1 and `green-light-500` is 2.18:1 on their surfaces. Steps 50 and 100 are surfaces; they are not meant to contrast with the page behind them, so `green-dark-50` against a dark page (`#0B0F14`) is about 1.05:1 by design.

Check any pairing outside this table before using it, including text on your neutral page background once that scale is defined.

## Dark scale calibration

Dark values are generated in OKLCH so every family follows the same lightness curve and steps stay comparable across hues. Lightness per step: 50 = 0.19, 100 = 0.23, 200 = 0.29, 300 = 0.42, 400 = 0.54, 500 = 0.65, 600 = 0.74, 700 = 0.82, 800 = 0.90, 900 = 0.95. Chroma is low for surfaces and text, highest in the middle, and clipped to the sRGB gamut. Hues are red 20°, amber 82° and green 150°, chosen so red and amber stay visibly apart.

These values are calibrated for WCAG contrast and perceptual consistency on screen. They are not calibrated for a specific clinical display or a measured room lighting condition. Check them on the target device before release. Because the families share lightness, red and green are hard to tell apart for people with red-green color blindness, so status must always carry an icon or label as well as color.

## Rules

- Text contrast: minimum 4.5:1 for body text and 3:1 for large text and meaningful UI components (WCAG 2.2 AA), checked separately in light and dark mode.
- Use `-text` for text and `-solid` for meaningful icons and indicators. Do not use steps 300 to 600 for either.
- Never use color as the only way to convey meaning; pair it with an icon, label or pattern.
- Maximum of [1] primary action color per view.
- Use semantic tokens in components. They resolve to the light or dark primitive for the active theme.
- Light and dark steps share the same role: 50 to 200 surfaces and borders, 300 to 600 decorative fills, 700 solid, 800 to 900 text.
- Only `green-light-700` to `green-light-900` are suitable for foreground text on light surfaces. `green-light-500` and `green-light-600` do not reach 4.5:1.

## Do and don't

<!-- Add examples of correct and incorrect color use in light and dark mode. -->

[Back to foundations](./README.md)
