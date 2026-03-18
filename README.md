# React-Vite-i18next-@tanstack/react-router-Tailwind-Example

This is an eaxmple how to create a project with React + Vite + i18next + Tailwind + @tanstack/react-router.

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
