# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install      # Install dependencies
npm run dev      # Start dev server at http://localhost:5173
npm run build    # Production build
npm run lint     # Run ESLint
npm run preview  # Preview production build
```

## Architecture

This is a minimal React + Vite single-page app with no backend, no routing, and no state management library.

- **`src/App.jsx`** — The entire application lives here: state, filtering logic, form handling, and all UI components are in one monolithic component.
- **`src/main.jsx`** — React entry point; mounts `<App />` to `#root`.
- State is managed with `useState`; no persistence (data resets on reload).

The app is a starter project intentionally containing bugs and poor code organization, meant to be improved as part of a course at codewithmosh.com.
