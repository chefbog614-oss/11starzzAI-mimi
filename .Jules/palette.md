## 2025-06-28 - Keyboard Accessibility and Shortcut Discoverability

**Learning:** Global keyboard shortcuts (e.g., 'T', 'L', 'R', 'B' for drawer toggles) significantly enhance power-user efficiency but must be implemented with a target check to avoid firing when a user is typing in form fields. Furthermore, these shortcuts remain "hidden" features unless visible hints (like `[T]`) are integrated directly into the UI labels.

**Action:** Always include a check for `input`, `textarea`, or `select` targets in global key listeners. Pair shortcuts with inline UI hints to ensure discoverability.

## 2025-06-28 - Semantic Buttons vs. Clickable Divs

**Learning:** Using generic `div` elements for interactive list items or triggers breaks keyboard accessibility (tabbing) and screen reader role identification.

**Action:** Use semantic `<button>` elements for all interactive triggers. Apply `w-full` and `text-left` utility classes to maintain layout consistency when replacing block-level `div` elements.
