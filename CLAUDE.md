# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static portfolio website for Manish Gurung. It presents resume information (education, skills, projects, work experience) as an interactive neural network visualization.

## Development

- **Entry point**: `index.html` (single file containing HTML, CSS, and JavaScript)
- **No build process**: Open `index.html` directly in a browser or serve with any static server
- **Quick serve**: `python -m http.server 8000` or `npx serve .`

## Architecture

The site uses a vanilla JS approach with no dependencies:

- **Data**: Resume content is stored in the `networkData` JavaScript object (line 352)
- **Rendering**: `renderLayers()` dynamically creates DOM elements for each neural network layer
- **Visualization**: SVG connections between neurons are drawn by `drawConnections()` using calculated coordinates
- **Interactivity**: Click neurons to open modals with detailed content; toggle sidebar via "IMPORTANT STUFF" button
- **Animation**: `animateSequence()` staggers layer activation with CSS transitions

## Key Sections to Modify

- **Contact info**: Lines 298-311 (sidebar)
- **Education/Skills**: Lines 365-372 (layer-2 in `networkData`)
- **Projects**: Lines 378-383 (layer-3 in `networkData`)
- **Work Experience**: Lines 389-391 (layer-4 in `networkData`)
- **Output/Bio**: Lines 397 (layer-5 in `networkData`)
- **Styling**: CSS variables defined at lines 9-43

## Color Scheme

Uses a teal/dark theme:
- `--c-onyx: #0a090c` (borders, text)
- `--c-dark-teal: #07393c` (headers, accents)
- `--c-stormy-teal: #2c666e` (hover states)
- `--c-frosted-blue: #90ddf0` (neurons)
- `--c-platinum: #f0edee` (sidebar background)
