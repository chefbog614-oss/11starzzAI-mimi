## 2026-06-08 - Enhancing Accessibility in Standalone HTML Projects

**Learning:** Standalone "megalithic" HTML files often lack basic accessibility structures like semantic buttons, ARIA regions, and proper label-input associations, making them difficult for screen reader users to navigate complex cyberpunk-themed dashboards.

**Action:** Always audit for non-semantic `div` elements used as buttons, ensure interactive drawers have `aria-expanded` and `aria-controls`, and use `aria-live` for dynamic log containers. Ensure all form labels are programmatically associated with inputs using the `for` attribute.

## 2025-06-30 - [Navigational Shortcuts & Hints]
**Learning:** For dashboards with off-screen panels (drawers), global keyboard shortcuts paired with visible hints (like `[L]`) significantly reduce interaction friction and improve accessibility for power users.
**Action:** Implement logical single-key shortcuts for navigation and use bracketed labels to make them discoverable.

## 2025-06-30 - [Input Shortcut Guard]
**Learning:** Global shortcuts must be explicitly guarded against `INPUT`, `TEXTAREA`, and `SELECT` elements to avoid breaking the core typing experience.
**Action:** Always check `event.target.tagName` before executing global key handlers.

## 2026-07-21 - [Characterful Mascot Hover and Focus Animations]
**Learning:** Adding characterful hover/focus animations to central mascot-style elements (like the Mascot Orb) makes the dashboard feel alive and interactive. Utilizing custom bezier transitions on pseudo-elements (like mascot ears) creates a delightful organic response when interactive states are active.
**Action:** Implement cubic-bezier(0.175, 0.885, 0.32, 1.275) scaling and rotational shifts on pseudo-elements during hover/focus to establish tactile visual feedback.
