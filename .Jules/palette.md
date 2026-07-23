## 2026-07-23 - Command History Buffer & Input Focus Controls

**Learning:** When building terminal-like features or shell environments inside web components, power users expect natural Command Line Interface (CLI) patterns such as command history navigation (ArrowUp/ArrowDown) and immediate focus via keybinds ('/'). To make this smooth, the cursor position must be explicitly managed, and a slight delay (e.g. 100ms) during slide-out drawer transitions is crucial to prevent focus trapping or incomplete focusing.

**Action:** Implement robust `setSelectionRange()` resets inside `setTimeout` when manipulating historical input values, and guard keyboard actions to ignore browser defaults and modify key bindings carefully.

## 2026-06-08 - Enhancing Accessibility in Standalone HTML Projects

**Learning:** Standalone "megalithic" HTML files often lack basic accessibility structures like semantic buttons, ARIA regions, and proper label-input associations, making them difficult for screen reader users to navigate complex cyberpunk-themed dashboards.

**Action:** Always audit for non-semantic `div` elements used as buttons, ensure interactive drawers have `aria-expanded` and `aria-controls`, and use `aria-live` for dynamic log containers. Ensure all form labels are programmatically associated with inputs using the `for` attribute.

## 2025-06-30 - [Navigational Shortcuts & Hints]
**Learning:** For dashboards with off-screen panels (drawers), global keyboard shortcuts paired with visible hints (like `[L]`) significantly reduce interaction friction and improve accessibility for power users.
**Action:** Implement logical single-key shortcuts for navigation and use bracketed labels to make them discoverable.

## 2025-06-30 - [Input Shortcut Guard]
**Learning:** Global shortcuts must be explicitly guarded against `INPUT`, `TEXTAREA`, and `SELECT` elements to avoid breaking the core typing experience.
**Action:** Always check `event.target.tagName` before executing global key handlers.
