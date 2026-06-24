# Palette Journal

## 2025-05-15 - Improving Drawer and Mascot Accessibility
**Learning:** In a cyberpunk-themed interface where custom elements like floating orbs or slide-out drawers are common, it is critical to use semantic buttons for interaction and ARIA attributes (aria-expanded, aria-controls) to disclose UI state. Standard CSS focus rings can clash with the aesthetic, so using custom focus-visible rings with box-shadow ensures both accessibility and visual consistency.
**Action:** Always convert interactive <div> elements to <button> and implement dynamic ARIA state management for collapsible UI components.
