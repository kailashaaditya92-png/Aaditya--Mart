# Aaditya Mart

Mobile-friendly online shopping starter for the existing `Aaditya--Mart` GitHub repository.

## Included
- Responsive Hindi/English storefront (navy, white, orange)
- Product search and category filters
- Cart with quantity controls and totals
- Supabase Auth sign-up/login wiring
- Supabase product read integration
- Demo admin inventory screen
- Starter SQL schema for products, customers, orders and order_items

## Run locally
1. Install Node.js (computer recommended for local development).
2. Run `npm install`
3. Copy `.env.example` to `.env` and fill in your Supabase Project URL and publishable/anon key.
4. Run `npm run dev`

## Mobile GitHub upload
1. Open the `Aaditya--Mart` repository in Chrome.
2. Tap **Add file** > **Upload files** (or use the `...` menu if the mobile layout hides it).
3. Upload all files and folders from this project ZIP, keeping folder names intact.
4. Commit changes to the `main` branch.

## Supabase setup
1. Open Supabase Dashboard > SQL Editor.
2. Run `supabase/schema.sql`.
3. In Supabase Project Settings > API, copy Project URL and the publishable key (or legacy anon key).
4. Set them in Vercel Environment Variables as `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY`.

## Important security / production work
This is a starter implementation, not a finished production store. The admin screen is a demo and is NOT access-controlled yet. Do not expose a service-role key in frontend code. The included SQL intentionally does not allow public product writes or direct order creation. Before accepting real payments/orders, implement secure server-side checkout and admin functions with role checks, server-side price validation, stock decrement, address/shipping fields, payment provider integration, and tests. Do not collect real customer data until these controls are complete.

## Current behavior without Supabase
The storefront works with sample products and a local demo cart. Login, database writes and real order creation require Supabase configuration and additional secure backend work.
