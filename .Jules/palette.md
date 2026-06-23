## 2025-05-14 - [Mascot Accessibility]
**Learning:** For central, branding-heavy "Launch" buttons often styled as custom graphics (like the mascot orb), using a semantic `<button>` instead of a `div` with a click listener is non-negotiable for keyboard and screen-reader accessibility.
**Action:** Always wrap branding-heavy interactive elements in `<button>` tags and provide clear `aria-label` and visual tooltips.

## 2025-05-14 - [Focus Ring Design]
**Learning:** Standard browser outlines can clash with neon-themed UI designs. A stacked `box-shadow` with an inner-glow effect can provide a high-visibility focus indicator that complements the aesthetic.
**Action:** Use stacked `box-shadow` (with a high-contrast offset) for focus-visible states in neon-themed applications.
