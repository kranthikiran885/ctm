# Deploy to Vercel via GitHub Integration (No CLI Needed)

Since disk space is limited locally, we'll use **Vercel's GitHub integration** to deploy directly from your repository without needing the CLI.

## Steps to Deploy

### 1. Go to Vercel Dashboard
- Open https://vercel.com/dashboard
- Log in (or sign up) with your GitHub account

### 2. Create New Project
- Click **"Add New"** → **"Project"**
- Select **"Import Git Repository"**

### 3. Import Your GitHub Repo
- Search for or paste: `kranthikiran885/ctm`
- Click **"Import"**

### 4. Configure Project Settings
When prompted, set:
- **Framework Preset:** `Next.js` (should auto-detect)
- **Root Directory:** `college-cosmos-home` (IMPORTANT!)
- **Build Command:** `pnpm install && pnpm build`
- **Install Command:** `pnpm install --frozen-lockfile`
- **Output Directory:** `.next` (auto-filled)

Click **"Continue"** or **"Deploy"** (varies by UI)

### 5. Set Environment Variables
Before deploying, you'll see an **"Environment Variables"** section:
- Click **"Add New"** for each variable:

| Key | Value | Scope |
|-----|-------|-------|
| NEXT_PUBLIC_API_URL | `https://your-backend-render-url.onrender.com` | Production, Preview, Development |
| NEXT_PUBLIC_APP_NAME | `College Cosmos Home` | Production, Preview, Development |
| NEXT_PUBLIC_APP_VERSION | `1.0.0` | Production, Preview, Development |
| NEXT_PUBLIC_SOCKET_URL | `https://your-socket-server.com` | Production, Preview, Development |
| NEXT_PUBLIC_GOOGLE_MAPS_API_KEY | `your-key-here` | Production, Preview, Development |
| NEXT_PUBLIC_VAPID_PUBLIC_KEY | `your-vapid-key` | Production, Preview, Development |
| NEXT_PUBLIC_GA_TRACKING_ID | `your-ga-id` | Production, Preview, Development |
| NEXT_PUBLIC_DEBUG | `false` | Production, Preview, Development |
| NODE_ENV | `production` | Production, Preview, Development |

### 6. Deploy
- Click **"Deploy"** button
- Wait 2-3 minutes for build to complete
- Once done, Vercel will show your live URL (e.g., `https://your-project.vercel.app`)

### 7. Test the Deployment
Visit your Vercel URL and test:
- ✅ Homepage loads (no 404)
- ✅ `/auth` page loads
- ✅ `/dashboard` page loads
- ✅ `/landing` page loads
- ✅ Check browser console for errors

## After Initial Deploy: Automatic Deployments

Vercel will **automatically redeploy** whenever you push to `main` branch:
1. Make code changes
2. Commit and push to GitHub
3. Vercel detects the push and automatically rebuilds
4. New version is live in seconds!

## If Deployment Fails

### Build Error: "Cannot find module 'X'"
- Check `college-cosmos-home/package.json` — all imports must be installed
- Verify Root Directory is set to `college-cosmos-home`

### Build Error: "ENOSPC: no space left on device"
- This is a Vercel infrastructure issue, rare and temporary
- Click **"Redeploy"** to retry

### 404 After Deployment
- Vercel handles SPA routing automatically
- Clear browser cache: `Ctrl+Shift+Delete`
- Try in incognito window
- Check build logs for errors

### API Calls Failing
- Verify `NEXT_PUBLIC_API_URL` points to your backend
- Check backend is running on Render
- Look at Network tab in DevTools to see actual requests

## Troubleshooting Environment Variables

If you see error like **"Secret 'api_url' does not exist"**:
1. Go to Project **Settings** → **Environment Variables**
2. **Delete** any invalid/incomplete variables
3. **Add fresh** variables with correct names (see table above)
4. Make sure to set scope to all three: Production, Preview, Development
5. Click **"Save"**
6. Go to **Deployments** → **Redeploy latest** → wait for rebuild

## Next Steps

1. ✅ Deploy via Vercel GitHub integration (above)
2. ✅ Test all routes load without 404
3. ✅ Verify API calls reach your backend (check Network tab)
4. ✅ Test authentication (signup/login flow)
5. Future: Set up custom domain (in Project Settings → Domains)

## Quick Reference: Your GitHub Repo
- **Owner:** kranthikiran885
- **Repo:** ctm
- **Branch:** main
- **Frontend Root:** college-cosmos-home/

---

**Status:** This is the fastest way to deploy without local CLI or disk space issues. Once connected to Vercel, all future pushes to `main` will auto-deploy! 🚀
