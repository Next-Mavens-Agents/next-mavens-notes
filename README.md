# Next Mavens Notes 📝

A secure, modern notes app with cloud storage and credential management.

## Features

- ✨ Beautiful gradient UI
- 🔐 Supabase authentication (sign up/sign in)
- 💾 Cloud storage via Supabase
- 🔑 Secure credential vault
- 📱 Fully responsive
- ⚡ Fast and lightweight
- 🛡️ Row-level security (users only see their own data)

## Quick Start

### 1. Set Up Supabase Database

Go to your [Supabase SQL Editor](https://app.supabase.com/project/yzatqexilcbvyprvbyra/sql/new) and run the SQL from `setup-supabase-sql.sql`.

This creates:
- `notes` table with RLS policies
- `credentials` table with RLS policies

### 2. Configure Supabase Keys

The app uses these Supabase credentials (already configured in index.html):

- **URL:** https://yzatqexilcbvyprvbyra.supabase.co
- **Anon Key:** (for client-side auth)
- **Service Role Key:** (for admin operations)

### 3. Run Locally

```bash
# Install dependencies
npm install

# Start local development server
npm start

# Open http://localhost:3000
```

### 4. Deploy to Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

## How It Works

### Authentication
- Sign up with email/password
- Stored in Supabase Auth
- User data isolated via Row-Level Security (RLS)

### Notes
- Create, edit, delete notes
- Stored in Supabase `notes` table
- Each note linked to user_id
- Only user can view/modify their notes

### Credentials Vault
- Store service credentials (API keys, tokens, passwords)
- Encrypted storage (at rest in Supabase)
- View/hide credential values
- Organize by service and type

## Security

- ✅ Supabase Auth for user management
- ✅ Row-Level Security (RLS) on all tables
- ✅ Only authenticated users can access data
- ✅ Users only see their own data
- ✅ Credentials hidden by default (click to reveal)

## Tech Stack

- HTML5
- CSS3 (with modern gradients and animations)
- Vanilla JavaScript
- Supabase (PostgreSQL + Auth)
- LocalStorage (fallback - not used in cloud mode)

## Development

Built by [Next Mavens](https://nextmavens.com) - Your Digital Solutions Partner

### Repository
https://github.com/Next-Mavens-Agents/next-mavens-notes

---

© 2026 Next Mavens. All rights reserved.
