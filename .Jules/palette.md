## 2025-07-03 - Accessible Spatial UI with Keyboard Shortcuts
**Learning:** In complex spatial interfaces with multiple drawers, global keyboard shortcuts (T, L, R, B) and visual hints (e.g., [L]) significantly improve discoverability and navigation efficiency.
**Action:** Always include keyboard shortcuts and visible hints when designing perimeter-based navigation systems.

## 2025-07-03 - Focus Management for Global Search/Shell
**Learning:** Using '/' as a global shortcut to focus a primary input is a well-received pattern, but it requires `e.preventDefault()` to avoid the character being typed into the input, and logic to ignore shortcuts when typing in other inputs.
**Action:** Use a standardized `keydown` handler that checks `event.target.tagName` and prevents default for focus-triggering shortcuts.

## 2026-07-04 - Global Escape for Spatial UI
**Learning:** In UIs with multiple overlapping or perimeter-based drawers, providing an 'Escape' key shortcut that closes all active panels provides a powerful and intuitive "reset" for the user's spatial context.
**Action:** Implement a global 'Escape' listener that iterates through all drawer states and ensures they are toggled closed.

## 2026-07-05 - Visual Feedback for Mascot Interactions
**Learning:** For central mascot or "hero" elements, adding subtle hover effects like scaling and brightness increases provides immediate tactile feedback that the element is interactive, even when it lacks a traditional button appearance.
**Action:** Incorporate `:hover` states with scale and brightness transformations for key interactive elements to provide tactile visual feedback for pointer users.

## 2026-07-06 - Command History in CLI-like Interfaces
**Learning:** For in-app terminal or shell components, implementing standard command history (ArrowUp/ArrowDown) significantly enhances productivity and aligns with user expectations from real CLI environments.
**Action:** Always implement a command history buffer for shell-like input components to allow quick re-execution of previous commands.
