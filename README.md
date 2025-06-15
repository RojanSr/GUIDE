# GUIDE to setup

Setting up react app. use this:-

```bash
pnpx create-tsrouter-app@latest
```

Check vite.config.ts file for any issue

If problem with path type:-
```bash
pnpm add -D @types/node
```

If problem with __dirname:-
```bash
const __dirname = dirname(fileURLToPath(import.meta.url))
```

If app is using deprecated like following:-
```bash
import { TanStackRouterVite } from '@tanstack/router-plugin/vite'
```
Replace with:-
```bash
import { tanstackRouter } from '@tanstack/router-plugin/vite'

 plugins: [
    tanstackRouter({
      target: 'react',
      autoCodeSplitting: true,
      verboseFileRoutes: false,
    }),
    react(),
  ],
```
