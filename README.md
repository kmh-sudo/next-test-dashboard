# Next.js Dashboard

A full-stack dashboard application built with Next.js 16, featuring authentication, invoice management, and customer tracking.

## Tech Stack

- **Framework:** Next.js 16 (Turbopack)
- **Language:** TypeScript
- **Styling:** Tailwind CSS 4
- **Authentication:** NextAuth.js v5
- **Database:** PostgreSQL (via `postgres` driver)
- **Validation:** Zod

## Prerequisites

- [Node.js](https://nodejs.org/) 18.18 or later
- [pnpm](https://pnpm.io/) package manager
- A PostgreSQL database (e.g., [Vercel Postgres](https://vercel.com/docs/storage/vercel-postgres))

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/kmh-sudo/next-test-dashboard.git
   cd dashboard
   ```

2. **Install dependencies**

   ```bash
   pnpm install
   ```

3. **Set up environment variables**

   Create a `.env` file in the root directory with the following variables:

   ```env
   POSTGRES_URL=your_postgres_connection_string
   AUTH_SECRET=your_auth_secret
   ```

   Generate an auth secret with:

   ```bash
   npx auth secret
   ```

4. **Seed the database**

   Start the dev server and visit `/seed` in your browser to populate the database with initial data:

   ```bash
   pnpm dev
   ```

   Then open [http://localhost:3000/seed](http://localhost:3000/seed).

5. **Run the development server**

   ```bash
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) in your browser.

## Scripts

| Command        | Description                  |
| -------------- | ---------------------------- |
| `pnpm dev`     | Start development server     |
| `pnpm build`   | Create production build      |
| `pnpm start`   | Start production server      |
| `pnpm lint`    | Run ESLint                   |

## Login Credentials

Use the following demo account to log in:

| Field    | Value                |
| -------- | -------------------- |
| Email    | `user@nextmail.com`  |
| Password | `123456`             |

## Deployment

This project is ready to deploy on [Vercel](https://vercel.com/). Connect your GitHub repository and Vercel will automatically build and deploy on push.

Make sure to add your environment variables (`POSTGRES_URL`, `AUTH_SECRET`) in the Vercel project settings.
