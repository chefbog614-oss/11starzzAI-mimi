## 2026-06-08 - Enhancing Accessibility in Standalone HTML Projects

**Learning:** Standalone "megalithic" HTML files often lack basic accessibility structures like semantic buttons, ARIA regions, and proper label-input associations, making them difficult for screen reader users to navigate complex cyberpunk-themed dashboards.

**Action:** Always audit for non-semantic `div` elements used as buttons, ensure interactive drawers have `aria-expanded` and `aria-controls`, and use `aria-live` for dynamic log containers. Ensure all form labels are programmatically associated with inputs using the `for` attribute.

## 2025-06-30 - [Navigational Shortcuts & Hints]
**Learning:** For dashboards with off-screen panels (drawers), global keyboard shortcuts paired with visible hints (like `[L]`) significantly reduce interaction friction and improve accessibility for power users.
**Action:** Implement logical single-key shortcuts for navigation and use bracketed labels to make them discoverable.

## 2025-06-30 - [Input Shortcut Guard]
**Learning:** Global shortcuts must be explicitly guarded against `INPUT`, `TEXTAREA`, and `SELECT` elements to avoid breaking the core typing experience.
**Action:** Always check `event.target.tagName` before executing global key handlers.

## 2026-07-26 - [Interactive Mascot and History Buffer Micro-UX]
**Learning:** Adding a command history buffer (ArrowUp/ArrowDown) to shell inputs coupled with a global Escape handler to close active drawers reduces repetitive user actions. Additionally, characterful hover/focus animations on mascot components (e.g., ear perking via cubic-bezier back-out transitions) make dashboards feel responsive and interactive.
**Action:** Implement ArrowUp/ArrowDown command history with setTimeout selection range resets and add custom CSS transition triggers for mascot elements on hover and focus-visible states.
