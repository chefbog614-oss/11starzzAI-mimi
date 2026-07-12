## 2025-05-14 - Terminal UX and Tactile Feedback
**Learning:** Command history buffer (ArrowUp/ArrowDown) is a fundamental expectation for terminal-like inputs, significantly reducing repetitive typing. Visual feedback on interactive mascots (hover/focus scaling) provides a tactile feel that makes the interface feel alive and responsive.
**Action:** Always implement history buffers for shell components and ensure primary interactive mascots have characterful secondary animations or state changes on interaction.

## 2025-05-15 - Defensive Shortcut Implementation
**Learning:** Global keyboard shortcuts (e.g., 'L', 'R') can easily collide with browser and OS-level commands (e.g., 'Ctrl+L' for address bar, 'Ctrl+R' for refresh). Failing to check for modifier keys leads to a frustrating user experience where standard navigation and tools are broken by the app's internal logic.
**Action:** When implementing global keydown listeners for shortcuts, always include a guard clause: `if (e.ctrlKey || e.altKey || e.metaKey) return;` unless specifically designing a chorded shortcut.
