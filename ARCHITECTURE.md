# LocalBite production architecture map

The ZIP now contains a complete demonstrable frontend plus a backend integration scaffold. The browser app still runs in demo mode using local storage; external credentials are not embedded.

## Product layers

1. Public marketing and SEO pages
2. Customer discovery, shop, cart, checkout, orders, account, favorites and QR flows
3. Vendor mobile-first workspace with menu, orders, kitchen, QR, tables, delivery, inventory, analytics, CRM, marketing, staff, support, billing and invoices
4. Admin operations for vendors, verification, orders, reviews, revenue, subscriptions, coupons, ads, delivery, sales agents, support, CMS, cities, audit logs and platform settings
5. Backend-ready PostgreSQL/Prisma schema and API surface
6. Vercel-ready SPA deployment configuration

## Integration boundaries

- Auth: secure session/OTP provider
- Payments: gateway + signed webhooks
- Maps: geocoding + distance/radius checks
- Storage: object storage for vendor/menu assets
- Notifications: push, SMS, WhatsApp and email
- Delivery: partner dispatch or first-party rider system
- Analytics: event pipeline
- Moderation: vendor/review/report tooling

The frontend labels these as demo/integration-ready where a live provider is required.
