# React-Vite-i18next-@tanstack/react-router-Tailwind-Example

This is an eaxmple how to create a project with React + Vite + i18next + Tailwind + @tanstack/react-router.

## ⚠️ Warning

> If you're trying to install dependencies with my current version of Vite, you might have issues with the compatibility of the dependencies. In this case, try to install the dependencies with the `--force` flag. Or you can try to create a project with older versions of Vite which do not have compatibility issues.

## Create a Project

Create a new project:

```bash
npm create vite@latest React-Vite-i18next-@tanstack/react-router-Tailwind-Example -- --template react-ts
```

## Install Talwind

Install Tailwind:

```bash
npm i tailwindcss @tailwindcss/vite
```

If you have issues with installing `@tailwindcss/vite`, then try:

```bash
npm i --force @tailwindcss/vite
```

Import `@tailwindcss/vite` in `vite.config.ts`:

```ts
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';
import tailwindcss from '@tailwindcss/vite';

// https://vite.dev/config/
export default defineConfig({
  plugins: [react(), tailwindcss()],
});
```

Import `tailwindcss` into `ìndex.css`:

```css
@import 'tailwindcss';
```

## Install @tanstack/react-router

Install @tanstack/react-router:

```bash
npm i @tanstack/react-router @tanstack/router-devtools
```

## Integrate `@tanstack/react-router`

Create `router.tsx`: [router.tsx](./src/router.tsx)

Then import the `AppRouter` into `main.tsx`:

```tsx
import { StrictMode } from 'react';
import { createRoot } from 'react-dom/client';

import './index.css';

import { AppRouter } from './router.tsx';

// import App from './App.tsx'

createRoot(document.getElementById('root')!).render(
  <StrictMode>
    <AppRouter />
  </StrictMode>,
);
```
