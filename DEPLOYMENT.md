# Deployment Guide

## Frontend Deployment (Vercel/Netlify)

### Vercel

1. Connect your GitHub repo to Vercel
2. Set environment variables in Vercel dashboard:
   ```
   VITE_API_URL=https://api.ttgt.in/api
   VITE_APP_NAME=TTGT Solutions
   ```
3. Deploy automatically on push to main

### Netlify

1. Connect GitHub repo
2. Build command: `cd frontend && npm run build`
3. Publish directory: `frontend/dist`
4. Set environment variables in Netlify UI
5. Deploy

## Backend Deployment (Railway/Heroku)

### Railway

1. Create new project on Railway
2. Connect GitHub repo
3. Add PostgreSQL plugin
4. Set environment variables:
   ```
   PORT=5000
   NODE_ENV=production
   DATABASE_URL=railway_postgres_url
   JWT_SECRET=strong_secret_key
   RESEND_API_KEY=your_key
   CLIENT_URL=https://ttgt.in
   ```
5. Deploy

### Heroku

1. Create Heroku app
2. Add PostgreSQL addon
3. Set config variables
4. Deploy via Git

## Database (Supabase)

1. Create Supabase project
2. Get connection string
3. Run migrations in Supabase SQL editor
4. Use connection string in environment

## Environment Variables

### Production

**Frontend (.env)**
```
VITE_API_URL=https://api.ttgt.in/api
VITE_APP_NAME=TTGT Solutions
```

**Backend (.env)**
```
PORT=5000
NODE_ENV=production
DATABASE_URL=postgresql://...
JWT_SECRET=very_strong_secret_key_here
JWT_EXPIRE=7d
RESEND_API_KEY=re_your_key
ADMIN_EMAIL=hello@ttgt.in
CLIENT_URL=https://ttgt.in
```

## SSL/HTTPS

- Vercel/Netlify provide free SSL
- Railway provides free SSL
- Set up custom domain via DNS

## Monitoring

- Use Railway/Vercel monitoring
- Set up error tracking (Sentry)
- Monitor database performance

## Backups

- Supabase provides automated backups
- Download backups regularly
- Test restore procedures

## Scaling

1. Monitor database performance
2. Enable caching for APIs
3. Optimize image sizes
4. Use CDN for static assets
5. Scale backend replicas as needed
