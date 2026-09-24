# LocalBite backend integration scaffold

The supplied frontend is a browser demo. This folder documents the production backend boundary so the UI can be connected without redesigning the product.

## Suggested stack

- Node.js / TypeScript API
- PostgreSQL
- Prisma ORM
- Zod validation
- Secure cookie/session authentication or a trusted auth provider
- Object storage for food/shop images
- Payment provider with signed webhooks
- Maps/geocoding provider
- Notification providers for SMS, WhatsApp, email and push

## API groups

`/auth` · `/users` · `/vendors` · `/locations` · `/menus` · `/catalog` · `/orders` · `/payments` · `/delivery` · `/tables` · `/qr` · `/reviews` · `/coupons` · `/promotions` · `/subscriptions` · `/ads` · `/analytics` · `/notifications` · `/support` · `/refunds` · `/sales-agents` · `/admin` · `/cms` · `/cities`

## Production rules

All role checks must happen server-side. Delivery eligibility and prices must be revalidated on the server. Payment status must come from verified webhooks rather than browser state. Uploaded files must be validated and stored outside the application bundle. Every mutation that affects money, roles, vendor status, refunds or audit-sensitive data should produce an audit event.
