# Accessibility

## Purpose

Accessibility is a requirement for every component and pattern in this system.

## Standard

WCAG [2.2] level [AA].

## Foundations

- **Keyboard:** every interactive element is reachable and operable by keyboard, in a logical order.
- **Focus:** visible focus indicator with at least [3:1] contrast on every interactive element.
- **Semantics:** use native elements first; ARIA only where native elements will not do.
- **Content:** alt text for meaningful images; labels for all form fields; error messages say what went wrong and how to fix it.

## Testing

[Automated tools, screen reader and keyboard pass] before release.

## Checklist

- [ ] Contrast meets the targets in [color](./color.md)
- [ ] Touch targets meet the minimum in [spacing and layout](./spacing-layout.md)
- [ ] Reduced motion is respected ([motion](./motion.md))
- [ ] Keyboard and screen reader tested

[Back to foundations](./README.md)
