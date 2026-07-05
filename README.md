# React + Vite

## Configuracion de API

El frontend usa `VITE_API_BASE_URL` para construir las llamadas al backend.

Para desarrollo local puedes copiar `.env.example` a `.env.local` y ajustar:

```env
VITE_API_BASE_URL=/api
VITE_DEV_API_PROXY_TARGET=http://127.0.0.1:8000
```

Con esa configuracion, Vite recibe llamadas a `/api/...` y las redirige al backend local.

Para produccion define `VITE_API_BASE_URL` en el entorno del build. Ejemplos:

```env
VITE_API_BASE_URL=https://api.tudominio.com/api
```

o, si el mismo dominio sirve el frontend y redirige `/api` al backend:

```env
VITE_API_BASE_URL=/api
```

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

