# LocalBite launch checklist

## Website deployment
- [ ] Connect the repository/project to Vercel
- [ ] Add custom domain
- [ ] Verify every public route on desktop and mobile
- [ ] Verify direct refresh on `/explore`, `/pricing`, `/vendor/...`, `/scan/...`
- [ ] Replace demo brand assets, contact details and social links

## Backend
- [ ] Production database
- [ ] Secure API
- [ ] User authentication / OTP
- [ ] Vendor role permissions
- [ ] Admin role permissions
- [ ] Audit logs
- [ ] Backups and recovery

## Payments & commerce
- [ ] Payment gateway
- [ ] Webhook signature verification
- [ ] Refund workflow
- [ ] Settlement / vendor payout workflow
- [ ] Invoices and taxes
- [ ] Coupon/discount rules
- [ ] Cancellation policy enforcement

## Food/vendor operations
- [ ] Vendor verification
- [ ] Applicable food registration/licence workflow
- [ ] Menu moderation
- [ ] Business-hours logic
- [ ] Delivery radius verification
- [ ] Order acceptance SLA
- [ ] Customer support escalation

## Delivery & location
- [ ] Real geolocation
- [ ] Maps / geocoding
- [ ] Server-side distance calculation
- [ ] Delivery fee calculation
- [ ] Delivery partner or dispatch system
- [ ] Live order status where offered

## Notifications
- [ ] SMS / OTP provider
- [ ] WhatsApp Business provider where appropriate
- [ ] Email provider
- [ ] Push notifications

## Security & quality
- [ ] Rate limiting
- [ ] Abuse/spam protection
- [ ] Secure file upload
- [ ] Error tracking
- [ ] Performance monitoring
- [ ] Privacy controls
- [ ] Data deletion / export process
- [ ] Legal review of terms, privacy and refund policy

This checklist is included so a browser prototype is not accidentally treated as a real payment/order backend.

## Frontend surfaces added in the latest build
- [ ] Customer solutions page
- [ ] Vendor solutions page
- [ ] Restaurant solutions page
- [ ] QR ordering page
- [ ] Table ordering page
- [ ] Blog / careers placeholders connected to routing
- [ ] Cookie policy / community guidelines pages
- [ ] Vendor orders queue
- [ ] Kitchen display board
- [ ] Delivery dispatch UI
- [ ] Inventory / sold-out controls
- [ ] Vendor reviews and invoices
- [ ] Admin verification, reviews, subscriptions, coupons, ads, delivery, sales agents, CMS, cities and audit views
- [ ] Customer saved addresses and payment-method preferences
- [ ] Backend Prisma schema and integration notes
