# Soft Unwind — Website Deployment Guide

## Files Included
- `index.html` — Landing / marketing page
- `privacy.html` — Privacy Policy (required by Apple)
- `support.html` — Support + FAQ (required by Apple)
- `terms.html` — Terms of Service
- `delete-account.html` — Account deletion (required if users have accounts)

---

## Option A: Deploy on Vercel (Recommended — Free, Fast)

1. Go to https://vercel.com and sign in (or create a free account)
2. Click **"Add New Project"** → drag your `softunwind` folder onto the page
3. Vercel will auto-detect it as a static site — no config needed
4. Click **Deploy** — you'll get a live URL like `softunwind.vercel.app`

**To connect your Squarespace domain to Vercel:**
1. In Vercel → your project → Settings → Domains
2. Add your custom domain (e.g., `softunwind.app`)
3. In Squarespace → Settings → Domains → [your domain] → DNS Settings
4. Add a CNAME record: `www` pointing to `cname.vercel-dns.com`
5. Add an A record: `@` pointing to `76.76.21.21`
6. Wait up to 24 hrs for DNS propagation

---

## Before Submitting to Apple — Checklist

Replace these placeholders in the HTML files first:

| Placeholder | Replace With |
|---|---|
| `[Your Name / Company Name]` | Your legal name or LLC name |
| `[Your State]` | Mississippi (or wherever you're incorporated) |
| `support@softunwind.app` | Your actual support email |

### Apple App Store Connect URLs to fill in:
- **Privacy Policy URL:** `https://yourdomain.com/privacy.html`
- **Support URL:** `https://yourdomain.com/support.html`
- **Marketing URL:** `https://yourdomain.com/`
- **Terms of Service URL (optional):** `https://yourdomain.com/terms.html`
- **Account Deletion URL:** `https://yourdomain.com/delete-account.html`

---

## Vercel CLI (fastest method if you have Node.js)

```bash
npm i -g vercel
cd softunwind
vercel
```
Follow the prompts — live in ~30 seconds.
