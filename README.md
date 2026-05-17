# OutOfStateNCInvestors.com
### Dennis Fields | Movement Mortgage | NMLS #1407951

Built with Astro + Tailwind CSS. Deployed on Vercel. Domain managed via Hostinger.

---

## 🔧 To Wire Your GHL Webhook

Open `src/pages/index.astro` and find this line:

```javascript
// In production: POST to GHL webhook or email provider here
console.log('Lead captured:', { name, email, market, budget });
```

Replace it with:

```javascript
await fetch('YOUR_GHL_WEBHOOK_URL_HERE', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name, email, market, budget })
});
```

## 📊 To Add Google Analytics

Find `</head>` in `src/pages/index.astro` and paste your GA4 script above it.

## 🌐 DNS Records for Hostinger

- A Record: `@` → `76.76.21.21` TTL 14400
- CNAME: `www` → `cname.vercel-dns.com` TTL 14400

---
All loans subject to approval. Equal Housing Lender.
