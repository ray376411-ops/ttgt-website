# Development Setup Guide

## Prerequisites

- Node.js 18+
- npm or yarn
- PostgreSQL (or Supabase account)
- Git

## Backend Setup

### 1. Clone and Install

```bash
cd backend
npm install
```

### 2. Environment Variables

Create `.env` file:

```env
PORT=5000
NODE_ENV=development

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/ttgt

# JWT
JWT_SECRET=your_super_secret_key_here
JWT_EXPIRE=7d

# Email
RESEND_API_KEY=your_resend_api_key
ADMIN_EMAIL=hello@ttgt.in

# CORS
CLIENT_URL=http://localhost:5173
```

### 3. Database Setup

```bash
# Create database
creatredb ttgt

# Run migrations
psql ttgt < ../database/schema.sql
```

### 4. Start Backend

```bash
npm run dev
```

Backend runs on `http://localhost:5000`

## Frontend Setup

### 1. Install Dependencies

```bash
cd frontend
npm install
```

### 2. Environment Variables

Create `.env` file:

```env
VITE_API_URL=http://localhost:5000/api
VITE_APP_NAME=TTGT Solutions
```

### 3. Start Development Server

```bash
npm run dev
```

Frontend runs on `http://localhost:5173`

## Project Structure

### Frontend Directories

- `src/components/` - Reusable React components
- `src/pages/` - Full page components
- `src/layouts/` - Layout wrapper components
- `src/services/` - API communication
- `src/hooks/` - Custom React hooks
- `src/context/` - React Context for state
- `src/styles/` - Global CSS & Tailwind

### Backend Directories

- `src/routes/` - Express route definitions
- `src/controllers/` - Request handlers
- `src/models/` - Database queries
- `src/middleware/` - Auth, validation
- `src/services/` - Business logic
- `src/config/` - Configuration

## Available Scripts

### Frontend

```bash
npm run dev      # Start dev server
npm run build    # Production build
npm run preview  # Preview build locally
npm run lint     # ESLint check
```

### Backend

```bash
npm run dev      # Start with nodemon
npm run start    # Production start
npm run lint     # ESLint check
```

## Database Migrations

To add new migrations:

1. Create SQL file in `migrations/`
2. Run: `psql ttgt < migrations/XXXX_description.sql`

## Testing

```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
```

## Troubleshooting

### Port Already in Use

```bash
# Find and kill process on port 5000
lsof -ti:5000 | xargs kill -9
```

### Database Connection Issues

- Verify DATABASE_URL is correct
- Check PostgreSQL is running
- Ensure database exists

### CORS Errors

- Check VITE_API_URL matches backend URL
- Verify CLIENT_URL in backend .env

## Next Steps

1. Start the backend server
2. Start the frontend dev server
3. Open http://localhost:5173 in browser
4. Navigate to /admin/login for admin panel
5. Check API.md for endpoint documentation
