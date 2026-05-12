# React to Vanilla HTML/CSS Migration Guide

## Overview
This document summarizes the workflow and steps taken to migrate a complex React/TypeScript/TailwindCSS landing page into standard HTML, CSS, and Vanilla JavaScript. The primary goal of this migration is to make the codebase fully compatible for integration with WordPress Elementor.

## Steps Performed
1. **Structural Analysis**: Reviewed the original `HomePage.tsx` to identify the distinct layout sections (e.g., Video Hero, News Ticker, Carousels, Timeline, Collage).
2. **CSS Decoupling**: 
   - Replaced Tailwind CSS utility classes with standard semantic CSS classes (e.g., `.typo-section-heading`, `.container`, `.portrait-card`).
   - Extracted brand colors, typography, and specific animations (like keyframes for fading and ticker scrolls) into a vanilla CSS stylesheet.
3. **HTML Construction**: 
   - Rebuilt the layout using standard HTML5 tags (`<section>`, `<div>`, `<button>`).
   - Hardcoded data arrays (`EVENTS`, `NOTICES`) that were previously mapped over in React directly into the HTML to ensure a 1:1 visual match.
4. **Vanilla JavaScript Implementation**: 
   - Converted React `useEffect` and `useRef` hooks handling scroll animations into standard `IntersectionObserver` logic.
   - Recreated the counter animation logic (previously a custom hook) using `requestAnimationFrame`.
   - Built a circular/wrap-around carousel logic for the Events and Notices grids using standard event listeners.
5. **Consolidation**: Merged the `<style>` block and `<script>` logic directly into the single `index.html` file to create a fully self-contained module.

## WordPress Elementor Integration Instructions
To successfully integrate this migrated HTML code into a WordPress page using Elementor, follow this exact setup hierarchy:

1. **Elementor Canvas**: Set your WordPress Page Layout to "Elementor Canvas" (this provides a clean slate without default theme headers/footers).
2. **Full Width Container**: Add a new Container onto the canvas and set its layout to "Full Width".
3. **HTML Widget**: Drag and drop Elementor's native "Custom HTML" widget inside that Full Width Container.
4. Paste the entire contents of `index.html` into the HTML Widget.
