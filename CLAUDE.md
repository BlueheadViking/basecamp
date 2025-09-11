# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Setup

This is a static HTML portfolio website hosted on GitHub Pages. No build tools, package managers, or development servers are required.

### Deployment
- Live site: https://grim.nz (configured via CNAME file)
- Hosted on GitHub Pages
- Direct deployment from main branch

### Testing Changes
Since this is a static site, simply open `index.html` in a browser to preview changes locally.

## Project Architecture

### File Structure
```
portfolio/
├── index.html          # Main portfolio page with navigation
├── styles.css          # All CSS styles and design system
├── CNAME              # GitHub Pages domain configuration
├── projects/          # Individual project case studies
├── experiments/       # Interactive experiments and demos
├── writing/           # Blog posts and articles
├── images/            # All visual assets
└── fonts/             # Custom font files
```

### Design System (styles.css)
- **CSS Variables**: Centralized color palette and design tokens in `:root`
- **Primary Colors**: `--background-color`, `--primary-color`, `--paragraph-color`, `--link-color`
- **Typography**: Custom fonts (ABCMonumentGrotesk, Figtree, JetBrains Mono)
- **Responsive Grid**: Auto-fit grid for project cards with 3D hover effects
- **Component Structure**: Modular CSS sections for buttons, cards, stats, navigation

### Content Navigation
The main page (index.html) uses JavaScript for:
- Smooth scrolling navigation between sections
- Dynamic routing to sub-pages based on `data-project` attributes:
  - Project cards → `projects/{project-name}.html`
  - Experiment rows → `experiments/{project-name}.html`
  - Writing rows → `writing/{project-name}.html`

### Interactive Features
- 3D hover effects on project cards (desktop only)
- Touch-friendly design with responsive breakpoints
- Material Icons integration for UI elements

## Content Management

### Adding New Projects
1. Create HTML file in appropriate directory (`projects/`, `experiments/`, or `writing/`)
2. Add corresponding entry in `index.html` with matching `data-project` attribute
3. Add thumbnail image to `images/` directory
4. Update project card or row with appropriate tags and description

### Image Optimization
- Thumbnails: PNG format for project cards
- Hero images: PNG/AVIF format for project pages
- Icons: SVG format for scalable graphics
- Background: SVG patterns for texture effects

### Typography Hierarchy
- H1: 48px (main hero title)
- H2: 32px (section headers)
- H3: 24px (stats numbers)
- H4: 18px (project titles)
- Body: 16px (Figtree for readability, JetBrains Mono for headers)