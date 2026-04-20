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

- **`src/App.jsx`** — Root component. Owns the `transactions` array state. Renders child components and passes props/callbacks down.
- **`src/Summary.jsx`** — Displays total income, total expenses, and balance. Receives `transactions` and computes totals internally.
- **`src/TransactionForm.jsx`** — Form for adding a new transaction. Owns its own local form state and calls the `onAdd` callback with the new transaction object on submit.
- **`src/TransactionList.jsx`** — Renders the transactions table with filter controls. Receives `transactions`, owns `filterType` and `filterCategory` state internally, and renders filtered rows via `Transaction`.
- **`src/Transaction.jsx`** — Renders a single transaction row (`<tr>`) in the transactions table. Receives a `transaction` prop.
- **`src/main.jsx`** — React entry point; mounts `<App />` to `#root`.

State is managed with `useState`; no persistence (data resets on reload).

The app is a starter project meant to be improved as part of a course at codewithmosh.com.
