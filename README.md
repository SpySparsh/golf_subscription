# Golf Subscription & Charity Platform ⛳

A full-stack, scalable subscription platform built to manage golf memberships, track player scores, and facilitate monthly charity prize draws. This application provides a seamless user experience for subscribers and a powerful, secure administrative dashboard for platform management.

## 🚀 Live Demo
**[Insert Your Live Vercel URL Here]**

## ✨ Key Features

### User Experience
* **Secure Authentication:** Passwordless/Credential login with secure session management.
* **Subscription Management:** Automated billing cycles, upgrades, and cancellations powered by the Stripe Customer Portal.
* **Charity Integration:** Users can view and select participating charities to support through their subscription.
* **Score Tracking:** Dedicated dashboard for users to log and track their golf scores.

### Admin Capabilities
* **Role-Based Access Control (RBAC):** Protected routes ensuring only authorized personnel can access the admin dashboard.
* **Draw Management:** Automated monthly prize pool calculations and winner selection.
* **Comprehensive Data Tables:** View and manage users, active subscriptions, charities, and historical winners.

### Technical Highlights
* **Modern React Architecture:** Built with Next.js 16 App Router utilizing Server Components for optimized performance and SEO.
* **Type Safety:** End-to-end TypeScript integration with database schema generation.
* **Webhook Synchronization:** Real-time database updates triggered by Stripe webhooks to ensure subscription statuses are always perfectly synced.
* **Automated Communications:** Transactional email routing via Resend.

## 🛠️ Tech Stack

* **Framework:** Next.js 16 (App Router)
* **Language:** TypeScript
* **Styling:** Tailwind CSS
* **Database & Auth:** Supabase (PostgreSQL)
* **Payments:** Stripe (Checkout & Billing)
* **Email:** Resend API
* **Deployment:** Vercel

## 📦 Getting Started

### Prerequisites
* Node.js 18+
* npm, yarn, pnpm, or bun

### 1. Clone the repository
```bash
git clone [https://github.com/SpySparsh/golf_subscription.git](https://github.com/SpySparsh/golf_subscription.git)
cd golf_subscription
```

2. Install dependencies
 ```
npm install
```
4. Configure Environment Variables
Create a .env.local file in the root directory and add the following keys. You will need to provision projects in Supabase, Stripe, and Resend to acquire these.

Code snippet
```
# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key

# Stripe Configuration
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret

# Resend Configuration
RESEND_API_KEY=your_resend_api_key

# App URL
NEXT_PUBLIC_APP_URL=http://localhost:3000
```
4. Run the development server
```
npm run dev
Open http://localhost:3000 with your browser to see the result.
```
🗄️ Database Schema Overview
The PostgreSQL database (managed via Supabase) relies on the following core tables:

profiles: Extended user data and RBAC flags (is_admin).

subscriptions: Syncs directly with Stripe subscription objects.

charities: Stores partnered charity details and allocations.

draws: Tracks monthly revenue, prize pools, and selected winners.

scores: Manages user-submitted golf scorecards.

👨‍💻 Author
Sparsh Sharma

GitHub: @SpySparsh

Portfolio: https://portfolio-teal-kappa-89.vercel.app/
