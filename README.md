# LocalBite — premium Vercel-ready product build

LocalBite is a hyperlocal food discovery + digital-shop + QR ordering + restaurant-management product concept.

## Product surfaces included

### Customer experience
- Premium landing page
- Nearby food discovery and filters
- Vendor/store pages
- Delivery / pickup / dine-in modes
- Single-vendor cart protection
- Demo checkout validation
- Order history
- Order tracking detail page
- Account and saved-shop preferences
- Favorites page
- QR scan experience
- Table QR context (`/scan/:vendorId?table=7`)
- English/Hindi global switch for the core customer/vendor UI

### Vendor experience
- Orders & fulfilment queue with status actions
- Kitchen display board
- Delivery dispatch workflow
- Inventory / sold-out controls
- Reviews & trust panel
- Invoice / printable receipt view
- Self onboarding or ₹99 assisted onboarding flow
- Five-step onboarding: shop, owner, universal menu, fulfilment, launch
- Owner verification/declaration fields
- Universal food catalog in English + Hindi
- Standard fallback item images + optional custom image selection
- Delivery radius: 1 / 3 / 5 km
- Self delivery, pickup and dine-in options
- Permanent digital-shop QR
- Table QR generation and download
- Vendor dashboard
- Catalog/menu management
- QR management
- Table ordering
- Analytics
- Customer view
- Marketing/campaign tools
- Team roles
- Support workflow
- Billing/plan view
- Vendor settings and language preferences

### Admin / business operations
- Vendor verification and trust queue
- Review moderation
- Subscription plan management
- Coupon / promotion management
- Advertising inventory and controls
- Delivery operations
- Sales executive network
- CMS / SEO content controls
- City rollout / service-area controls
- Audit-log view
- Platform overview
- Vendor pipeline
- Orders
- Revenue streams
- Support queue
- Platform settings
- Featured/sponsored listing model
- Risk checklist / production integration checklist

### Public product pages
- For customers
- For vendors
- Restaurant solutions
- QR ordering
- Table ordering
- Blog
- Careers
- Cookie policy
- Community guidelines
- Features
- Pricing
- How it works
- FAQ
- About
- Contact
- Support
- Privacy template
- Terms template
- Refund/cancellation template
- Login / signup demo

## Demo behavior
The website is intentionally self-contained and stores demo data in browser `localStorage`, so the main flows can be explored without a backend.

Demo OTP: `1234`

## Launch architecture
The frontend is a Vite + React SPA and includes a Vercel SPA rewrite. Deploying it on Vercel should use:
- Build command: `npm run build`
- Output directory: `dist`
- Node: 20+

## Production work still required before accepting real public transactions
This is the important line between a product prototype and a real business launch. Connect and test these before real customers pay or real vendors are onboarded at scale:

1. Production database and API (for vendors, menus, customers, orders, tables, payouts and audit logs).
2. Real authentication/OTP provider, role-based authorization and secure session handling.
3. Payment gateway, webhook verification, refunds, settlement/reconciliation and invoices.
4. Maps/location provider and server-side distance/radius checks.
5. Real delivery partner workflow or your own dispatch system.
6. Real push/SMS/WhatsApp/email notifications.
7. Vendor KYC/food-business verification and your final compliance workflow.
8. Tax/accounting setup, terms, privacy policy and refund policy reviewed for the actual operating entity.
9. Production monitoring, error tracking, rate limiting, abuse prevention and backups.
10. Custom domain, business email, support number and analytics.
11. Replace demo content, placeholder social links and demo metrics.
12. Configure your real pricing, commission, onboarding and promotional commercial terms.

No frontend-only package should be described as a fully production-safe payment platform until those backend and operational pieces are connected and tested.

## Local run

```bash
npm install
npm run dev
```

## Vercel

Import the project into Vercel. The included `vercel.json` handles SPA route refreshes. The project also contains a web manifest and basic robots file.

## Backend integration scaffold

The ZIP also includes `ARCHITECTURE.md` plus `backend/README.md`, `backend/.env.example` and a PostgreSQL/Prisma schema at `backend/prisma/schema.prisma`. These define the production data model and API boundaries without pretending that a database, payment gateway, OTP service, maps provider or delivery network is already connected.

## Validation performed on the packaged source

The final source was checked for JSX/JavaScript syntax by transpiling the React entry file with the installed TypeScript compiler and running Node's syntax checker on the generated JavaScript. A full Vite production build could not be executed in this environment because the npm dependency registry is not reachable, so `node_modules` was not installed here.
