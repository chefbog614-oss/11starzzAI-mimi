# Palette Journal

## 2025-05-15 - Improving Drawer and Mascot Accessibility
**Learning:** In a cyberpunk-themed interface where custom elements like floating orbs or slide-out drawers are common, it is critical to use semantic buttons for interaction and ARIA attributes (aria-expanded, aria-controls) to disclose UI state. Standard CSS focus rings can clash with the aesthetic, so using custom focus-visible rings with box-shadow ensures both accessibility and visual consistency.
**Action:** Always convert interactive <div> elements to <button> and implement dynamic ARIA state management for collapsible UI components.

## 2025-06-25 - [Async Console Accessibility]
**Learning:** For terminal-style interfaces that log asynchronous agent activity, `aria-live="polite"` is essential for keeping screen reader users informed without interrupting their current task.
**Action:** Always apply `aria-live="polite"` to containers where dynamic logs or status updates are appended.

## 2025-06-25 - [Keyboard Shortcut Visibility]
**Learning:** Productivity-enhancing keyboard shortcuts (like '/' for focus) are invisible to users unless prompted. Including them in placeholders or tooltips significantly improves discoverability.
**Action:** Append keyboard shortcut hints in parentheses to input placeholders or related tooltips.
