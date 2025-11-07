# Fix Vercel Environment Variable Error

## Problem
`Environment Variable "NEXT_PUBLIC_API_URL" references Secret "api_url", which does not exist.`

## Solution

### Option 1: Direct Value (Recommended)
In Vercel Dashboard → Environment Variables:

```
Name: NEXT_PUBLIC_API_URL
Value: https://your-backend-url.herokuapp.com
Environment: Production
```

### Option 2: Create the Secret First
1. Go to Vercel Dashboard → Settings → Environment Variables
2. Click "Add New"
3. Name: `api_url`
4. Value: `https://your-backend-url.herokuapp.com`
5. Save as Secret
6. Then reference it: `@api_url`

### Quick Fix Commands
```bash
# Remove existing env vars
vercel env rm NEXT_PUBLIC_API_URL

# Add new one with direct value
vercel env add NEXT_PUBLIC_API_URL
# Enter: https://your-backend-url.herokuapp.com

# Redeploy
vercel --prod
```

### Required Environment Variables
```
NEXT_PUBLIC_API_URL=https://your-backend-url.herokuapp.com
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_maps_key
NODE_ENV=production
```