# Studio — creative services booking (college project)
Setup: `npm i && cp .env.example .env.local` (fill BUSINESS_NOTIFICATION_EMAIL, RESEND_API_KEY, ADMIN_PASSWORD) then `npm run dev`.
Demo: Login > "Use demo account" > search "YouTube" > Add > search "website" > Add > Cart > Checkout > Place order > Simulate ₹2 payment > Admin (ADMIN_PASSWORD).
Orders persist in data/orders.json (local demo storage, not a production DB). Without Resend keys the email status honestly shows "not_configured" and can be retried in Admin.

## Deploy to Netlify
1. Supabase: create a project, run supabase/schema.sql in the SQL editor.
2. Push this folder to GitHub, then Netlify > Add new site > Import from Git (build: `npm run build`).
3. Netlify > Site settings > Environment variables: add every key from .env.example (secrets pasted only there).
4. Redeploy. Admin password = ADMIN_PASSWORD. Resend's onboarding sender only delivers to your own Resend signup email.
