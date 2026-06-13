# TTGT Solutions - E-commerce Growth Platform

**Think Today, Grow Tomorrow**

A complete production-ready website and admin dashboard for TTGT Solutions, a company that helps offline retail businesses scale online across India's top e-commerce marketplaces.

## 🚀 Tech Stack

### Frontend
- **React 18** + **Vite** - Lightning-fast development
- **Tailwind CSS** - Modern utility-first styling
- **React Router v6** - Client-side routing
- **Framer Motion** - Smooth animations
- **Lucide React** - Icon library
- **Axios** - HTTP client

### Backend
- **Node.js + Express** - RESTful API
- **PostgreSQL (Supabase)** - Database
- **JWT Authentication** - Secure auth
- **Resend** - Email notifications

## 📋 Project Structure

```
ttgt-website/
├── frontend/                 # React + Vite application
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── pages/           # Page components
│   │   ├── layouts/         # Layout components
│   │   ├── hooks/           # Custom hooks
│   │   ├── services/        # API services
│   │   ├── context/         # React context
│   │   ├── styles/          # Global styles
│   │   └── App.jsx
│   ├── public/              # Static assets
│   ├── package.json
│   ├── vite.config.js
│   └── tailwind.config.js
├── backend/                 # Express API
│   ├── src/
│   │   ├── routes/          # API routes
│   │   ├── controllers/     # Route handlers
│   │   ├── models/          # Database models
│   │   ├── middleware/      # Auth, validation
│   │   ├── services/        # Business logic
│   │   ├── config/          # Configuration
│   │   └── index.js
│   ├── migrations/          # Database migrations
│   ├── package.json
│   └── .env.example
├── database/                # Database schema
│   └── schema.sql
└── docs/                    # Documentation
    ├── DEPLOYMENT.md
    ├── API.md
    └── SETUP.md
```

## 🎨 Design System

- **Primary Background**: #0A0A0B (Deep Black)
- **Surface**: #161618 (Dark Gray)
- **Accent**: #FF5C00 (Vibrant Orange)
- **Text**: White
- **Theme**: Premium Black SaaS with Glassmorphism

## 📱 Public Website Pages

1. **Home** - Hero section with brand story
2. **Services** - 9 core services in modern cards
3. **Process** - 6-step timeline workflow
4. **Benefits** - Key value propositions
5. **Team** - Professional team profiles
6. **Contact** - Lead capture form
7. **Footer** - Links and company info

## 🛠️ Admin Dashboard Features

- **Dashboard** - KPI cards & overview analytics
- **Leads Management** - Status tracking & follow-ups
- **Client Management** - Client profiles & history
- **Store Management** - Marketplace store tracking
- **Product Management** - Product listings
- **Order Management** - Order tracking & fulfillment
- **Ad Performance** - Campaign analytics
- **Revenue Analytics** - Business metrics
- **Team Management** - Staff profiles
- **Settings** - System configuration

## 🔐 Authentication

- JWT-based authentication
- Role-based access control (Super Admin, Admin, Manager)
- Protected admin routes
- Secure token refresh mechanism

## 📧 Email System

When a lead is created via the contact form:
1. Lead saved to database
2. Email sent to hello@ttgt.in with lead details
3. Lead appears in admin dashboard

## 🚢 Deployment

- Frontend: Vercel/Netlify ready
- Backend: Heroku/Railway ready
- Database: Supabase PostgreSQL
- Environment-based configuration

## 📚 Documentation

- See `SETUP.md` for local development
- See `API.md` for backend endpoints
- See `DEPLOYMENT.md` for production deployment

## 📄 License

Copyright © 2024 TTGT Solutions. All rights reserved.
