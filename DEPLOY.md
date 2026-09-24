# Vercel deployment

1. Upload/import this folder into a Git repository or directly into Vercel.
2. Framework preset: **Vite**.
3. Build command: `npm run build`.
4. Output directory: `dist`.
5. Node.js: 20 or newer.
6. Add a custom domain after the first successful deployment.
7. Test these routes after deployment: `/`, `/explore`, `/onboard`, `/vendor-dashboard`, `/admin`, `/scan/v1`, `/pricing`, `/faq`, `/contact`.

## SPA refreshes

`vercel.json` rewrites all routes to `/index.html`, so client-side React Router URLs continue to work when refreshed.

## Before public launch

This ZIP is a self-contained frontend product prototype. Connect production authentication, API/database, payments, tax/invoices, maps, delivery, notifications, vendor verification, analytics and legal documents before taking real orders or money.
