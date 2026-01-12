# Vercel Deployment Guide

## Quick Deployment Steps

### Option 1: Vercel Dashboard (Easiest)

1. Push your code to GitHub
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import your repository
4. Vercel auto-detects Vite configuration
5. Click "Deploy"

### Option 2: Vercel CLI

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Login to Vercel:
```bash
vercel login
```

3. Deploy:
```bash
vercel
```

4. For production:
```bash
vercel --prod
```

## Configuration

All configuration is handled automatically through:
- `vercel.json` - Deployment settings, SPA routing, caching headers
- `vite.config.js` - Build optimization
- `package.json` - Build scripts

## Environment Variables

If you need to add environment variables:

1. Go to your project on Vercel Dashboard
2. Settings → Environment Variables
3. Add your variables (e.g., VITE_FORMSPREE_ID)

## Custom Domain

1. Go to your project on Vercel
2. Settings → Domains
3. Add your custom domain
4. Follow DNS configuration instructions

## Automatic Deployments

- Every push to `main` branch triggers production deployment
- Pull requests get preview deployments
- Instant rollbacks available from Vercel Dashboard

## Performance

Vercel provides:
- ✅ Global CDN
- ✅ Automatic HTTPS
- ✅ Image optimization
- ✅ Edge caching
- ✅ Zero-config deployment

## Monitoring

View analytics and logs at:
- Deployments: [vercel.com/dashboard](https://vercel.com/dashboard)
- Analytics: Project → Analytics tab
- Logs: Project → Deployments → View Function Logs
