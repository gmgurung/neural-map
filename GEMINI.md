# GEMINI.md

This file provides foundational mandates and instructional context for Gemini CLI when working in this repository. These instructions take absolute precedence over general workflows.

## Project Overview

This is a static portfolio website for Manish Gurung, designed as an interactive "Neural Profile Network." It presents professional information (education, skills, projects, work experience) through a dynamic, neural network-inspired visualization.

- **Primary Technologies**: HTML5, CSS3 (Vanilla), JavaScript (Vanilla).
- **Architecture**: Single-file application (`index.html`) with no external dependencies or build steps.
- **Key Features**: 
  - Dynamic rendering of neural network layers.
  - SVG-based connections between "neurons."
  - Modal-based content display for detailed resume items.
  - Interactive sidebar and theme toggling (Light/Dark mode).

## Building and Running

Since this is a static project, no build process is required.

- **Run Locally**: Open `index.html` directly in any modern web browser.
- **Serve with HTTP**:
  - Python: `python -m http.server 8000`
  - Node.js: `npx serve .`
- **Testing**: Manual verification in a browser is the primary testing method. Ensure responsiveness and interactivity across different screen sizes.

## Development Conventions

- **Single File Structure**: All HTML, CSS, and JS are contained within `index.html`.
- **Data Management**: Resume content is managed via the `networkData` object within the `<script>` tag.
- **Styling**: 
  - Uses CSS Variables (`:root`) for easy theme management.
  - Adheres to a specific color palette (Onyx, Platinum, Dark Teal, Frosted Blue).
  - Dark mode is supported via the `[data-theme="dark"]` selector.
- **Code Organization**:
  - **CSS**: Lines 9-330 approx.
  - **HTML Structure**: Lines 335-350 approx.
  - **JavaScript Logic**: Lines 352+ (includes data, rendering logic, and event listeners).

## Key Modification Points

- **Contact/Sidebar Info**: Located near line 298.
- **Resume Data**: The `networkData` object (around line 352) is the source of truth for all displayed content.
- **Visuals**: SVG connection logic is handled by `drawConnections()`.
- **Styling**: Modify the `:root` variables at the top of the file to change the global theme.
