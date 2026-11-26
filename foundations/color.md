# Color

## Purpose

Color in this system has two separate jobs. Brand colors (teal and vivid teal) carry identity and emphasis. Feedback colors (red, amber, green) carry clinical status and risk. Every palette has a light and a dark scale so interfaces stay legible in both themes.

<!-- Add a screenshot of your palettes here. -->

## Theme modes

Every palette is defined twice: `[hue]-light-[step]` and `[hue]-dark-[step]`. Steps keep the same role in both modes (see [tokens](./tokens.md#theme-modes)), so components use semantic tokens and never reference a mode directly.

| Steps | Role in both modes |
|---|---|
| 50 to 200 | Surfaces, tints and borders |
| 300 to 600 | Decorative fills. Not for text or required graphics |
| 700 | Solid: icons, indicators and fills behind on-solid text |
| 800 to 900 | Text |

## Brand colors

Brand colors express identity and emphasis: key actions, links, selected states and brand moments. They never signal status. Error, warning and success use the [feedback colors](#feedback-colors), and a brand color must not stand in for one of them.

Both brand palettes follow the same light and dark step roles as every other palette, so components use the semantic tokens below and never reference a mode directly.

### Brand primary: Teal

Anchor: `#00677F` at step 700 (`teal-light-700`). It is 6.47:1 on white, so it works as a solid with white or step 50 text on top.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | <img src="./assets/swatches/EBF8FC.svg" width="14" height="14" alt="EBF8FC swatch"> `#EBF8FC` | <img src="./assets/swatches/09161A.svg" width="14" height="14" alt="09161A swatch"> `#09161A` | Teal 50 | Surface | Tinted brand background |
| 100 | <img src="./assets/swatches/D6F0FA.svg" width="14" height="14" alt="D6F0FA swatch"> `#D6F0FA` | <img src="./assets/swatches/0B2027.svg" width="14" height="14" alt="0B2027 swatch"> `#0B2027` | Teal 100 | Subtle surface | Subtle surface and hover tint |
| 200 | <img src="./assets/swatches/B7E3F2.svg" width="14" height="14" alt="B7E3F2 swatch"> `#B7E3F2` | <img src="./assets/swatches/113039.svg" width="14" height="14" alt="113039 swatch"> `#113039` | Teal 200 | Border | Hover state and decorative border |
| 300 | <img src="./assets/swatches/88D1E9.svg" width="14" height="14" alt="88D1E9 swatch"> `#88D1E9` | <img src="./assets/swatches/125568.svg" width="14" height="14" alt="125568 swatch"> `#125568` | Teal 300 | Decorative | Illustrations and chart backgrounds |
| 400 | <img src="./assets/swatches/59B9D7.svg" width="14" height="14" alt="59B9D7 swatch"> `#59B9D7` | <img src="./assets/swatches/1E7A93.svg" width="14" height="14" alt="1E7A93 swatch"> `#1E7A93` | Teal 400 | Decorative | Illustrations and chart series |
| 500 | <img src="./assets/swatches/1FA1C4.svg" width="14" height="14" alt="1FA1C4 swatch"> `#1FA1C4` | <img src="./assets/swatches/319DBC.svg" width="14" height="14" alt="319DBC swatch"> `#319DBC` | Teal 500 | Decorative | High-emphasis decorative fill |
| 600 | <img src="./assets/swatches/1584A1.svg" width="14" height="14" alt="1584A1 swatch"> `#1584A1` | <img src="./assets/swatches/5FB9D5.svg" width="14" height="14" alt="5FB9D5 swatch"> `#5FB9D5` | Teal 600 | Decorative | Strong accent, decorative only |
| 700 | <img src="./assets/swatches/00677F.svg" width="14" height="14" alt="00677F swatch"> `#00677F` | <img src="./assets/swatches/88D1E9.svg" width="14" height="14" alt="88D1E9 swatch"> `#88D1E9` | Teal 700 | Brand primary | Brand primary anchor (<img src="./assets/swatches/00677F.svg" width="14" height="14" alt="00677F swatch"> `#00677F`). Buttons, links, selected states |
| 800 | <img src="./assets/swatches/044D5F.svg" width="14" height="14" alt="044D5F swatch"> `#044D5F` | <img src="./assets/swatches/BBE6F6.svg" width="14" height="14" alt="BBE6F6 swatch"> `#BBE6F6` | Teal 800 | Text | Brand-colored text on tinted surfaces |
| 900 | <img src="./assets/swatches/08333F.svg" width="14" height="14" alt="08333F swatch"> `#08333F` | <img src="./assets/swatches/DDF3FB.svg" width="14" height="14" alt="DDF3FB swatch"> `#DDF3FB` | Teal 900 | Strong text | Highest-emphasis brand text |

Token names: `teal-light-50` to `teal-light-900`, `teal-dark-50` to `teal-dark-900`.

### Brand secondary: Vivid Teal

Anchor: `#00A4B3` at step 500 (`vivid-teal-light-500`). It is only 3.02:1 on white. Use it for graphics, illustration and large elements, never for body text. Step 700 is the solid for interactive secondary elements.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | <img src="./assets/swatches/EAF8FA.svg" width="14" height="14" alt="EAF8FA swatch"> `#EAF8FA` | <img src="./assets/swatches/081618.svg" width="14" height="14" alt="081618 swatch"> `#081618` | Vivid Teal 50 | Surface | Tinted brand background |
| 100 | <img src="./assets/swatches/D5F1F5.svg" width="14" height="14" alt="D5F1F5 swatch"> `#D5F1F5` | <img src="./assets/swatches/092124.svg" width="14" height="14" alt="092124 swatch"> `#092124` | Vivid Teal 100 | Subtle surface | Subtle surface and hover tint |
| 200 | <img src="./assets/swatches/B5E5EB.svg" width="14" height="14" alt="B5E5EB swatch"> `#B5E5EB` | <img src="./assets/swatches/0E3135.svg" width="14" height="14" alt="0E3135 swatch"> `#0E3135` | Vivid Teal 200 | Border | Hover state and decorative border |
| 300 | <img src="./assets/swatches/83D3DE.svg" width="14" height="14" alt="83D3DE swatch"> `#83D3DE` | <img src="./assets/swatches/065860.svg" width="14" height="14" alt="065860 swatch"> `#065860` | Vivid Teal 300 | Decorative | Illustrations and chart backgrounds |
| 400 | <img src="./assets/swatches/50BDCA.svg" width="14" height="14" alt="50BDCA swatch"> `#50BDCA` | <img src="./assets/swatches/0D7D89.svg" width="14" height="14" alt="0D7D89 swatch"> `#0D7D89` | Vivid Teal 400 | Decorative | Illustrations and chart series |
| 500 | <img src="./assets/swatches/00A4B3.svg" width="14" height="14" alt="00A4B3 swatch"> `#00A4B3` | <img src="./assets/swatches/00A4B3.svg" width="14" height="14" alt="00A4B3 swatch"> `#00A4B3` | Vivid Teal 500 | Brand secondary | Brand secondary anchor (<img src="./assets/swatches/00A4B3.svg" width="14" height="14" alt="00A4B3 swatch"> `#00A4B3`). Graphics and large elements only; 3.02:1 on white |
| 600 | <img src="./assets/swatches/098793.svg" width="14" height="14" alt="098793 swatch"> `#098793` | <img src="./assets/swatches/57BCC8.svg" width="14" height="14" alt="57BCC8 swatch"> `#57BCC8` | Vivid Teal 600 | Decorative | Strong accent, decorative only |
| 700 | <img src="./assets/swatches/026973.svg" width="14" height="14" alt="026973 swatch"> `#026973` | <img src="./assets/swatches/83D3DE.svg" width="14" height="14" alt="83D3DE swatch"> `#83D3DE` | Vivid Teal 700 | Solid | Actions and indicators; on-solid text is step 50 |
| 800 | <img src="./assets/swatches/024F56.svg" width="14" height="14" alt="024F56 swatch"> `#024F56` | <img src="./assets/swatches/B8E8EE.svg" width="14" height="14" alt="B8E8EE swatch"> `#B8E8EE` | Vivid Teal 800 | Text | Brand-colored text on tinted surfaces |
| 900 | <img src="./assets/swatches/02353A.svg" width="14" height="14" alt="02353A swatch"> `#02353A` | <img src="./assets/swatches/DCF4F7.svg" width="14" height="14" alt="DCF4F7 swatch"> `#DCF4F7` | Vivid Teal 900 | Strong text | Highest-emphasis brand text |

Token names: `vivid-teal-light-50` to `vivid-teal-light-900`, `vivid-teal-dark-50` to `vivid-teal-dark-900`.

### Brand semantic mapping

| Semantic token | Light mode | Dark mode | Usage |
|---|---|---|---|
| `color-brand-[role]-surface` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Tinted brand background, for example a selected row or an info panel |
| `color-brand-[role]-border` | `{[hue]-light-200}` | `{[hue]-dark-200}` | Decorative divider. A control that relies on its border alone must use the solid token |
| `color-brand-[role]-solid` | `{[hue]-light-700}` | `{[hue]-dark-700}` | Brand fills and meaningful indicators (3:1 or more against the surface): buttons, links, selected states |
| `color-brand-[role]-on-solid` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Text and icons placed on the solid color |
| `color-brand-[role]-text` | `{[hue]-light-800}` | `{[hue]-dark-800}` | Brand-colored text on the surface, subtle surface and hover surface |
| `color-brand-secondary-accent` | `{vivid-teal-light-500}` | `{vivid-teal-dark-500}` | Decorative accent only. Do not use for text or as the only indicator (3.02:1 on white) |

Roles and hues: `primary` uses `teal`, `secondary` uses `vivid-teal`. For example, `color-brand-primary-solid` is `{teal-light-700}` in light mode and `{teal-dark-700}` in dark mode.

### Brand contrast check

WCAG 2.2 AA ratios for every pairing the brand semantic tokens create, calculated from the hex values above. Text needs 4.5:1. Meaningful icons and indicators need 3:1.

| Pairing | Requirement | Teal light | Teal dark | Vivid Teal light | Vivid Teal dark |
|---|---|---|---|---|---|
| Text (800) on surface (50) | 4.5:1 | 8.68 | 13.81 | 8.56 | 13.89 |
| Text (800) on subtle surface (100) | 4.5:1 | 7.93 | 12.61 | 7.86 | 12.61 |
| Text (800) on hover surface (200) | 4.5:1 | 6.85 | 10.47 | 6.82 | 10.48 |
| Solid (700) on surface (50) | 3:1 | 5.96 | 10.82 | 5.90 | 10.84 |
| On-solid (50) on solid (700) | 4.5:1 | 5.96 | 10.82 | 5.90 | 10.84 |

All pairings pass in both modes. Steps 300 to 600 are decorative and are not guaranteed to meet 3:1 or 4.5:1. `vivid-teal-light-500` is 3.02:1 on white, which meets 3:1 for graphics but not 4.5:1 for text.

## Neutral palette

| Role | Token | Light value | Dark value | Usage |
|---|---|---|---|---|
| Neutral scale | `neutral-[light/dark]-[50-900]` | [#] | [#] | [Text, borders, surfaces] |

## Feedback colors

Feedback colors communicate risk and state: error, warning and success. They are separate from the brand colors above and are never used for branding or decoration. An info color is not defined yet (`color-feedback-info`: [#] light, [#] dark).

### Red: error and critical

Namespace `clinical.vitals.red`. Reference standard: ISO 3864 / IEC 60601.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | <img src="./assets/swatches/FFF0F2.svg" width="14" height="14" alt="FFF0F2 swatch"> `#FFF0F2` | <img src="./assets/swatches/210D0D.svg" width="14" height="14" alt="210D0D swatch"> `#210D0D` | Clinical Pink | Low Risk | Low-severity backgrounds, safe observation bounds |
| 100 | <img src="./assets/swatches/FFCCD3.svg" width="14" height="14" alt="FFCCD3 swatch"> `#FFCCD3` | <img src="./assets/swatches/2F1314.svg" width="14" height="14" alt="2F1314 swatch"> `#2F1314` | Clinical Rose | Mild Alert | Attention indicator, borderline diagnostic values |
| 200 | <img src="./assets/swatches/FFA2A2.svg" width="14" height="14" alt="FFA2A2 swatch"> `#FFA2A2` | <img src="./assets/swatches/451E1F.svg" width="14" height="14" alt="451E1F swatch"> `#451E1F` | Medical Coral | Moderate | Moderate severity warnings, pending clinical review |
| 300 | <img src="./assets/swatches/FF3B30.svg" width="14" height="14" alt="FF3B30 swatch"> `#FF3B30` | <img src="./assets/swatches/7E2F33.svg" width="14" height="14" alt="7E2F33 swatch"> `#7E2F33` | Arterial Red | Arterial | Oxygenated blood flow, standard critical boundary |
| 400 | <img src="./assets/swatches/D12626.svg" width="14" height="14" alt="D12626 swatch"> `#D12626` | <img src="./assets/swatches/B54249.svg" width="14" height="14" alt="B54249 swatch"> `#B54249` | Venous Red | Venous | Deoxygenated blood, lab classification standards |
| 500 | <img src="./assets/swatches/E60000.svg" width="14" height="14" alt="E60000 swatch"> `#E60000` | <img src="./assets/swatches/E45B63.svg" width="14" height="14" alt="E45B63 swatch"> `#E45B63` | Critical Red | Critical | Immediate vitals warning, patient risk threshold |
| 600 | <img src="./assets/swatches/C20000.svg" width="14" height="14" alt="C20000 swatch"> `#C20000` | <img src="./assets/swatches/F68486.svg" width="14" height="14" alt="F68486 swatch"> `#F68486` | Emergency | Emergency | Life-critical failure states, system stop triggers |
| 700 | <img src="./assets/swatches/990000.svg" width="14" height="14" alt="990000 swatch"> `#990000` | <img src="./assets/swatches/FEAAA9.svg" width="14" height="14" alt="FEAAA9 swatch"> `#FEAAA9` | Biohazard Red | Biohazard | Active hazard zoning, infectious agent presence |
| 800 | <img src="./assets/swatches/6D000D.svg" width="14" height="14" alt="6D000D swatch"> `#6D000D` | <img src="./assets/swatches/FBD3D2.svg" width="14" height="14" alt="FBD3D2 swatch"> `#FBD3D2` | Clinical Maroon | Deep Maroon | Secondary trend failures, pathology classification |
| 900 | <img src="./assets/swatches/2F0004.svg" width="14" height="14" alt="2F0004 swatch"> `#2F0004` | <img src="./assets/swatches/FEE9E8.svg" width="14" height="14" alt="FEE9E8 swatch"> `#FEE9E8` | Near-Black Red | Extreme Alert | Extreme clinical crisis, imminent danger status |

Token names: `red-light-50` to `red-light-900`, `red-dark-50` to `red-dark-900`.

### Amber: warning and caution

Governs caution indicators, pending triage queues, medium-risk vitals and non-fatal medication interaction flags. Tuned for optical comfort in low-light hospital environments.

| Step | Light value | Dark value | Name | Level | Usage |
|---|---|---|---|---|---|
| 50 | <img src="./assets/swatches/FFFDF2.svg" width="14" height="14" alt="FFFDF2 swatch"> `#FFFDF2` | <img src="./assets/swatches/1C1202.svg" width="14" height="14" alt="1C1202 swatch"> `#1C1202` | Amber 50 | Informational | Soft clinical cream for backgrounds |
| 100 | <img src="./assets/swatches/FEFCE8.svg" width="14" height="14" alt="FEFCE8 swatch"> `#FEFCE8` | <img src="./assets/swatches/271A01.svg" width="14" height="14" alt="271A01 swatch"> `#271A01` | Amber 100 | Low Caution | Light amber for low-caution alerts |
| 200 | <img src="./assets/swatches/FEF3C7.svg" width="14" height="14" alt="FEF3C7 swatch"> `#FEF3C7` | <img src="./assets/swatches/3A2800.svg" width="14" height="14" alt="3A2800 swatch"> `#3A2800` | Amber 200 | Mild Alert | Secondary attention, non-urgent states |
| 300 | <img src="./assets/swatches/FDE68A.svg" width="14" height="14" alt="FDE68A swatch"> `#FDE68A` | <img src="./assets/swatches/644701.svg" width="14" height="14" alt="644701 swatch"> `#644701` | Amber 300 | Pending | Warm amber for pending status and tasks |
| 400 | <img src="./assets/swatches/FCD34D.svg" width="14" height="14" alt="FCD34D swatch"> `#FCD34D` | <img src="./assets/swatches/8E6704.svg" width="14" height="14" alt="8E6704 swatch"> `#8E6704` | Amber 400 | Moderate Warning | Standard clinical amber for alerts |
| 500 | <img src="./assets/swatches/F59E0B.svg" width="14" height="14" alt="F59E0B swatch"> `#F59E0B` | <img src="./assets/swatches/B78500.svg" width="14" height="14" alt="B78500 swatch"> `#B78500` | Amber 500 | Elevated Risk | Deep amber for active caution flags |
| 600 | <img src="./assets/swatches/D97706.svg" width="14" height="14" alt="D97706 swatch"> `#D97706` | <img src="./assets/swatches/D6A12B.svg" width="14" height="14" alt="D6A12B swatch"> `#D6A12B` | Amber 600 | High Caution | Burnt amber for persistent risk status |
| 700 | <img src="./assets/swatches/B45309.svg" width="14" height="14" alt="B45309 swatch"> `#B45309` | <img src="./assets/swatches/E5BE77.svg" width="14" height="14" alt="E5BE77 swatch"> `#E5BE77` | Amber 700 | Urgent Review | Dark amber for immediate clinical checks |
| 800 | <img src="./assets/swatches/92400E.svg" width="14" height="14" alt="92400E swatch"> `#92400E` | <img src="./assets/swatches/EDDCBD.svg" width="14" height="14" alt="EDDCBD swatch"> `#EDDCBD` | Amber 800 | Severe Caution | Near-brown amber for critical delays |
| 900 | <img src="./assets/swatches/451A03.svg" width="14" height="14" alt="451A03 swatch"> `#451A03` | <img src="./assets/swatches/F7EDDC.svg" width="14" height="14" alt="F7EDDC swatch"> `#F7EDDC` | Amber 900 | Severe Risk | Extreme dark amber warning threshold |

Token names: `amber-light-50` to `amber-light-900`, `amber-dark-50` to `amber-dark-900`.

### Green: success and pass

Specification: Standards v4.2. Used for healthy physiological signs, within-threshold lab results, verified authorization states and validated medical devices.

| Step | Light value | Dark value | Name | Example | Usage |
|---|---|---|---|---|---|
| 50 | <img src="./assets/swatches/F0FDF4.svg" width="14" height="14" alt="F0FDF4 swatch"> `#F0FDF4` | <img src="./assets/swatches/07180B.svg" width="14" height="14" alt="07180B swatch"> `#07180B` | Normal BG | Patient Chart BG | Soft clinical mint for background states |
| 100 | <img src="./assets/swatches/DCFCE7.svg" width="14" height="14" alt="DCFCE7 swatch"> `#DCFCE7` | <img src="./assets/swatches/0B2311.svg" width="14" height="14" alt="0B2311 swatch"> `#0B2311` | In Range | Vitals Safe Zone | Light green for safe within-range highlights |
| 200 | <img src="./assets/swatches/BBF7D0.svg" width="14" height="14" alt="BBF7D0 swatch"> `#BBF7D0` | <img src="./assets/swatches/11331B.svg" width="14" height="14" alt="11331B swatch"> `#11331B` | Healthy | Optimal BMI Stat | Spring green for optimal healthy indicators |
| 300 | <img src="./assets/swatches/86EFAC.svg" width="14" height="14" alt="86EFAC swatch"> `#86EFAC` | <img src="./assets/swatches/0B5D2A.svg" width="14" height="14" alt="0B5D2A swatch"> `#0B5D2A` | Pass | Lab Test Cleared | Standard clinical green for pass and cleared |
| 400 | <img src="./assets/swatches/4ADE80.svg" width="14" height="14" alt="4ADE80 swatch"> `#4ADE80` | <img src="./assets/swatches/02853C.svg" width="14" height="14" alt="02853C swatch"> `#02853C` | Cleared | Discharge Approved | Medium green for verified normal ranges |
| 500 | <img src="./assets/swatches/22C55E.svg" width="14" height="14" alt="22C55E swatch"> `#22C55E` | <img src="./assets/swatches/1EAB53.svg" width="14" height="14" alt="1EAB53 swatch"> `#1EAB53` | Verified | EHR Auth Confirmed | Deep green for confirmed safe parameters |
| 600 | <img src="./assets/swatches/16A34A.svg" width="14" height="14" alt="16A34A swatch"> `#16A34A` | <img src="./assets/swatches/62C37A.svg" width="14" height="14" alt="62C37A swatch"> `#62C37A` | Approved | Device Connected | Forest green for strong verified states |
| 700 | <img src="./assets/swatches/15803D.svg" width="14" height="14" alt="15803D swatch"> `#15803D` | <img src="./assets/swatches/95D7A2.svg" width="14" height="14" alt="95D7A2 swatch"> `#95D7A2` | Confirmed | Identity Matched | Dark green for absolute clinical cleared |
| 800 | <img src="./assets/swatches/166534.svg" width="14" height="14" alt="166534 swatch"> `#166534` | <img src="./assets/swatches/CAE7CF.svg" width="14" height="14" alt="CAE7CF swatch"> `#CAE7CF` | Safe | Critical Safe Alert | Deep forest for high-contrast safety text |
| 900 | <img src="./assets/swatches/14532D.svg" width="14" height="14" alt="14532D swatch"> `#14532D` | <img src="./assets/swatches/E3F4E6.svg" width="14" height="14" alt="E3F4E6 swatch"> `#E3F4E6` | Absolute | Final Sign-off | Near-black green for absolute verification |

Token names: `green-light-50` to `green-light-900`, `green-dark-50` to `green-dark-900`.

### Feedback semantic mapping

| Semantic token | Light mode | Dark mode | Usage |
|---|---|---|---|
| `color-feedback-[role]-surface` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Tinted background of an alert or status container |
| `color-feedback-[role]-border` | `{[hue]-light-200}` | `{[hue]-dark-200}` | Decorative divider. A control that relies on its border alone must use the solid token |
| `color-feedback-[role]-solid` | `{[hue]-light-700}` | `{[hue]-dark-700}` | Status icons and indicators (3:1 or more against the surface) |
| `color-feedback-[role]-on-solid` | `{[hue]-light-50}` | `{[hue]-dark-50}` | Text and icons placed on the solid color |
| `color-feedback-[role]-text` | `{[hue]-light-800}` | `{[hue]-dark-800}` | Text on the surface, subtle surface and hover surface |

Roles and hues: `error` uses `red`, `warning` uses `amber`, `success` uses `green`. For example, `color-feedback-error-text` is `{red-light-800}` in light mode and `{red-dark-800}` in dark mode.

### Feedback contrast check

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

### Feedback dark scale calibration

Dark values of the feedback palettes are generated in OKLCH so every family follows the same lightness curve and steps stay comparable across hues. Lightness per step: 50 = 0.19, 100 = 0.23, 200 = 0.29, 300 = 0.42, 400 = 0.54, 500 = 0.65, 600 = 0.74, 700 = 0.82, 800 = 0.90, 900 = 0.95. Chroma is low for surfaces and text, highest in the middle, and clipped to the sRGB gamut. Hues are red 20°, amber 82° and green 150°, chosen so red and amber stay visibly apart.

These values are calibrated for WCAG contrast and perceptual consistency on screen. They are not calibrated for a specific clinical display or a measured room lighting condition. Check them on the target device before release. Because the families share lightness, red and green are hard to tell apart for people with red-green color blindness, so status must always carry an icon or label as well as color.

## Rules

- Text contrast: minimum 4.5:1 for body text and 3:1 for large text and meaningful UI components (WCAG 2.2 AA), checked separately in light and dark mode.
- Use `-text` for text and `-solid` for meaningful icons and indicators. Do not use steps 300 to 600 for either.
- Never use color as the only way to convey meaning; pair it with an icon, label or pattern.
- Keep brand and feedback colors apart: brand colors never signal status, and feedback colors never serve as brand or decoration.
- Maximum of [1] primary action color per view.
- Use semantic tokens in components. They resolve to the light or dark primitive for the active theme.
- Light and dark steps share the same role: 50 to 200 surfaces and borders, 300 to 600 decorative fills, 700 solid, 800 to 900 text.
- Only `green-light-700` to `green-light-900` are suitable for foreground text on light surfaces. `green-light-500` and `green-light-600` do not reach 4.5:1.

## Do and don't

<!-- Add examples of correct and incorrect color use in light and dark mode. -->

[Back to foundations](./README.md)
