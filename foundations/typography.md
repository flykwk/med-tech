# Typography

## Purpose

Typography makes clinical information readable at a glance, shows what matters most through a clear hierarchy, and keeps the interface calm and professional.

<!-- Add a type specimen screenshot here. -->

## Typefaces

- **Primary:** [Font name] for [UI / headings]
- **Secondary:** [Font name] for [body / data]
- **Fallback stack:** [system fonts]

## Type scale

| Style | Token | Size / Line height | Weight | Usage |
|---|---|---|---|---|---|
| Display | `display-xl` | 48 / 56 | Bold | Single critical value, such as a dose or heart rate on a monitor |
| Display | `display-lg` | 32 / 40 | Bold | Key vitals and KPI tiles |
| Display | `display-md` | 24 / 32 | Semibold | Secondary readings |
| Heading 1 | `h1` | 24 / 32 | Semibold | Screen title |
| Heading 2 | `h2` | 20 / 28 | Semibold | Panel title |
| Heading 3 | `h3` | 16 / 24 | Semibold | Section title |
| Heading 3 | `h4` | 14 / 20 | Semibold | Group or table title |
| Body | `body-lg` | 16 / 24 | Regular | Instructions and long text |
| Body | `body` | 14 / 20 | Regular | Default for forms and tables |
| Body | `body-sm` | 12 / 16 | Regular | Secondary text, with 12px as the floor |
| Label | `label` | 14 /20 | Medium | Field labels, buttons, menu items |
| Label | `label-sm` | 12 / 16 | Medium | Badges, units, column headers |
| Caption | `caption` | [ ] | [ ] | [Helper text, metadata] |
| Code | `code` | 13 / 20 | Regular, monospace | Device IDs, logs, DICOM tags |

## Rules

- Body text never smaller than [16px / 14px for dense UI].
- Nothing goes below 12px.
- Line length: aim for 45–75 characters per line in reading text.
- Limit to [2] typefaces and [4] weights.
- Use relative units (rem) so text scales with user settings.
- Use tabular (fixed-width) figures for every number, so values don't shift as they update.
- Alarm and safety text is never smaller than body, and is never set in color alone.
- Units use a lighter or smaller style next to the value, for example display-lg for "72" and label for "bpm".
- Layouts must survive 200% text resize.
- Emphasis comes from the semibold variant, not from a new style.

## Do and don't

<!-- Add examples of correct and incorrect type use. -->

[Back to foundations](./README.md)
