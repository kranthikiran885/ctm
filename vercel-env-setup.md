# Vercel Environment Variables Setup

## Required Environment Variables for Production

### 1. Vercel Dashboard Setup
Go to your Vercel project → Settings → Environment Variables

### 2. Add these variables:

```bash
# API Configuration
NEXT_PUBLIC_API_URL=https://your-backend-api.herokuapp.com
NEXT_PUBLIC_APP_NAME=College Cosmos Home
NEXT_PUBLIC_APP_VERSION=1.0.0

# Google Maps API
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_api_key

# Push Notifications
NEXT_PUBLIC_VAPID_PUBLIC_KEY=your_vapid_public_key

# Socket.io Server
NEXT_PUBLIC_SOCKET_URL=https://your-socket-server.herokuapp.com

# Analytics (Optional)
NEXT_PUBLIC_GA_TRACKING_ID=G-XXXXXXXXXX

# Environment
NODE_ENV=production
NEXT_PUBLIC_DEBUG=false
```

### 3. Deployment Commands

```bash
# Build and deploy
npm run build
vercel --prod

# Or auto-deploy via GitHub integration
git push origin main
```

### 4. Environment Variable Types

- **NEXT_PUBLIC_*** - Exposed to browser (client-side)
- **Regular vars** - Server-side only (API routes)

### 5. Security Notes

- Never expose sensitive keys with NEXT_PUBLIC_ prefix
- Use different API keys for production vs development
- Enable CORS on your backend for your domain only