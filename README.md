# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and Oxlint's TypeScript related rules in your project.


## Laboratory Exercise 4 – Guide Questions

### 1. Why do we use two separate states, searchText and debouncedSearch?

We use two states because searchText stores what the user is currently typing, while debouncedSearch stores the search value after waiting 300 milliseconds. This helps prevent unnecessary updates while typing.

### 2. What would happen if the debounce effect did not return a cleanup function?

Without a cleanup function, previous timers would not be cancelled. This could cause unnecessary updates and multiple timers running at the same time.

### 3. What is the purpose of the dependency array?

The dependency array tells React when an effect should run. An empty array means the effect runs after the initial render, while leaving it out makes the effect run after every render.

### 4. Why should we avoid sorting the original products array directly?

We should avoid sorting the original array because sort() changes the original data. We use the spread operator to create a copy before sorting.

### 5. Is the filtered product list better stored in its own state, or calculated from existing state during rendering?

It is better to calculate the filtered product list during rendering because it depends on existing state values. This avoids unnecessary state updates and keeps the data consistent.
