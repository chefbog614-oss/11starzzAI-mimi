## 2026-06-08 - Enhancing Accessibility in Standalone HTML Projects

**Learning:** Standalone "megalithic" HTML files often lack basic accessibility structures like semantic buttons, ARIA regions, and proper label-input associations, making them difficult for screen reader users to navigate complex cyberpunk-themed dashboards.

**Action:** Always audit for non-semantic `div` elements used as buttons, ensure interactive drawers have `aria-expanded` and `aria-controls`, and use `aria-live` for dynamic log containers. Ensure all form labels are programmatically associated with inputs using the `for` attribute.

## 2025-06-30 - [Navigational Shortcuts & Hints]
**Learning:** For dashboards with off-screen panels (drawers), global keyboard shortcuts paired with visible hints (like `[L]`) significantly reduce interaction friction and improve accessibility for power users.
**Action:** Implement logical single-key shortcuts for navigation and use bracketed labels to make them discoverable.

## 2025-06-30 - [Input Shortcut Guard]
**Learning:** Global shortcuts must be explicitly guarded against `INPUT`, `TEXTAREA`, and `SELECT` elements to avoid breaking the core typing experience.
**Action:** Always check `event.target.tagName` before executing global key handlers.

## 2025-07-25 - [Terminal Command History & Focus Navigation]
**Learning:** Implementing Up/Down arrow key command history buffers aligns terminal inputs with real CLI/Shell behaviors, satisfying developer user instincts. Paired with global Escape handler and shortcut modifier keys guard, this keeps the keyboard interaction flows fluid and natural.
**Action:** Track shell command histories in local storage/variables and bind ArrowUp/ArrowDown on keydown event listener. Ensure `setTimeout` of 0 is used to properly place the input cursor at the end. Protect browser shortcuts with modifier key guards.
