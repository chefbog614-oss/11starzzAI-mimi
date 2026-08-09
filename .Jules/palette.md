## 2026-06-08 - Enhancing Accessibility in Standalone HTML Projects

**Learning:** Standalone "megalithic" HTML files often lack basic accessibility structures like semantic buttons, ARIA regions, and proper label-input associations, making them difficult for screen reader users to navigate complex cyberpunk-themed dashboards.

**Action:** Always audit for non-semantic `div` elements used as buttons, ensure interactive drawers have `aria-expanded` and `aria-controls`, and use `aria-live` for dynamic log containers. Ensure all form labels are programmatically associated with inputs using the `for` attribute.

## 2025-06-30 - [Navigational Shortcuts & Hints]
**Learning:** For dashboards with off-screen panels (drawers), global keyboard shortcuts paired with visible hints (like `[L]`) significantly reduce interaction friction and improve accessibility for power users.
**Action:** Implement logical single-key shortcuts for navigation and use bracketed labels to make them discoverable.

## 2025-06-30 - [Input Shortcut Guard]
**Learning:** Global shortcuts must be explicitly guarded against `INPUT`, `TEXTAREA`, and `SELECT` elements to avoid breaking the core typing experience.
**Action:** Always check `event.target.tagName` before executing global key handlers.

## 2026-06-09 - Terminal Command History Buffer & Escape Key Panel Guard
**Learning:** Implementing ArrowUp/ArrowDown command navigation history significantly reduces interaction friction for CLI or terminal elements, aligning with user expectations for terminal-like components. Globally-bound Escape key handlers that close all open perimeter drawers and blur active inputs restore the primary viewport focus efficiently.
**Action:** Use an internal command history array with index tracking, and always use setTimeout with selection range to ensure the cursor stays at the end when the value is updated. For Escape, loop over drawer states to close them and call `.blur()` on the active element.
