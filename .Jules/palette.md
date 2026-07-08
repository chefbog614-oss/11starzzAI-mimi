## 2025-07-03 - Accessible Spatial UI with Keyboard Shortcuts
**Learning:** In complex spatial interfaces with multiple drawers, global keyboard shortcuts (T, L, R, B) and visual hints (e.g., [L]) significantly improve discoverability and navigation efficiency.
**Action:** Always include keyboard shortcuts and visible hints when designing perimeter-based navigation systems.

## 2025-07-03 - Focus Management for Global Search/Shell
**Learning:** Using '/' as a global shortcut to focus a primary input is a well-received pattern, but it requires `e.preventDefault()` to avoid the character being typed into the input, and logic to ignore shortcuts when typing in other inputs.
**Action:** Use a standardized `keydown` handler that checks `event.target.tagName` and prevents default for focus-triggering shortcuts.

## 2026-07-04 - Global Escape for Spatial UI
**Learning:** In UIs with multiple overlapping or perimeter-based drawers, providing an 'Escape' key shortcut that closes all active panels provides a powerful and intuitive "reset" for the user's spatial context.
**Action:** Implement a global 'Escape' listener that iterates through all drawer states and ensures they are toggled closed.

## 2026-07-07 - Command History for Web Shells
**Learning:** Users expect CLI-like behavior in web-based diagnostic shells. Implementing a command history buffer (ArrowUp/ArrowDown) significantly improves the UX by allowing rapid re-execution of complex commands.
**Action:** Implement a history array and index pointer for any terminal-like input components.

## 2026-07-08 - Tactile Hover Feedback for Mascot/Avatars
**Learning:** Adding subtle, characterful animations (like ears perking) alongside standard scaling and glow effects on hover for mascot-like interactive elements makes the interface feel more "alive" and responsive.
**Action:** Use CSS `::before`/`::after` transitions to add secondary animations to mascot components.
