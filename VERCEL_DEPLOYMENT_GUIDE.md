# Deploy College Cosmos to Vercel (Next.js Optimized)

Vercel is the best platform for Next.js applications. It provides:
- ✅ Automatic Optimizations for Next.js
- ✅ Zero-config Deployments
- ✅ Built-in SPA Routing (no manual _redirects needed)
- ✅ Global CDN
- ✅ Automatic HTTPS

## Quick Deployment Steps

### Step 1: Create Free Vercel Account
1. Go to https://vercel.com/signup
2. Sign up with GitHub (recommended)
3. Authorize Vercel to access your GitHub account

### Step 2: Import Your Repository
1. After signup, click **"Add New..."** → **"Project"**
2. Select **"Import Git Repository"**
3. Paste your GitHub URL: `https://github.com/kranthikiran885/ctm`
4. Click **"Import"**

### Step 3: Configure Project Settings
1. **Framework Preset:** Select **"Next.js"** (should auto-detect)
2. **Root Directory:** Set to **`college-cosmos-home`**
3. **Build Command:** `pnpm install && pnpm build`
4. **Install Command:** `pnpm install --frozen-lockfile`
5. **Output Directory:** `.next` (auto-set)

### Step 4: Set Environment Variables
1. Click **"Environment Variables"** section
2. Add these variables:
   ```
   NEXT_PUBLIC_API_URL = https://your-backend-url.onrender.com
   NEXT_PUBLIC_APP_NAME = College Cosmos Home
   NEXT_PUBLIC_APP_VERSION = 1.0.0
   NEXT_PUBLIC_SOCKET_URL = https://your-backend-url.onrender.com
   NEXT_PUBLIC_DEBUG = false
   NODE_ENV = production
   ```
3. Select **"Production"** for environment

### Step 5: Deploy
1. Click **"Deploy"** button
2. Wait for build to complete (usually 2-3 minutes)
3. Once complete, you'll see your live URL like: `https://your-project.vercel.app`

### Step 6: Test Your Site
- Homepage: https://your-project.vercel.app
- Auth page: https://your-project.vercel.app/auth
- Dashboard: https://your-project.vercel.app/dashboard
- Landing: https://your-project.vercel.app/landing

All routes should work without 404 errors!

## Why Vercel Over Netlify?

| Feature | Vercel | Netlify |
|---------|--------|---------|
| Next.js Optimization | ✅ Native | ⚠️ Requires Config |
| SPA Routing | ✅ Auto | ⚠️ Manual _redirects |
| Build Time | ⚠️ ~2-3 min | ⚠️ ~2-3 min |
| Edge Functions | ✅ Yes | ✅ Yes |
| Free Tier | ✅ Good | ✅ Good |
| Support | ✅ Excellent | ✅ Good |

## Troubleshooting

### Build Fails on Vercel
- Check build logs in Vercel dashboard
- Verify all dependencies in package.json
- Ensure root directory is set to `college-cosmos-home`

### Still Getting 404 Errors
- Vercel automatically handles SPA routing
- No need for _redirects file (unlike Netlify)
- Clear browser cache and try incognito window

### Custom Domain
1. Go to Project Settings
2. Click **"Domains"**
3. Add your custom domain
4. Update DNS records as instructed

## Production Checklist

- [ ] Vercel deployment shows "Ready"
- [ ] Homepage loads without 404
- [ ] All routes work (/auth, /dashboard, /landing, etc.)
- [ ] Environment variables are set correctly
- [ ] API calls go to backend (check Network tab)
- [ ] Real-time updates work (Socket.IO)
- [ ] No console errors in DevTools

## Next Steps

1. Update `NEXT_PUBLIC_API_URL` with your actual Render backend URL
2. Test authentication flow
3. Monitor build logs for any issues
4. Set up automatic deployments (already enabled with GitHub)

## Support

For Vercel issues:
- Documentation: https://vercel.com/docs
- Support: https://vercel.com/support

Enjoy your deployed application! 🚀
