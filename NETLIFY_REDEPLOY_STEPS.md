# Netlify Redeploy Steps to Fix 404 Error

## Problem
Frontend is deployed but showing 404 error. The _redirects file and netlify.toml fixes have been committed and pushed to GitHub, but Netlify hasn't redeployed with these changes.

## Solution: Manual Redeploy with Cache Clear

### Step 1: Go to Netlify Dashboard
- Open https://app.netlify.com
- Log in with your credentials

### Step 2: Select the transportvucse Site
- Look for "transportvucse" in your sites list
- Click on it to open the site dashboard

### Step 3: Navigate to Deploys
- Click on the **"Deploys"** tab in the top navigation
- You'll see a list of all deployments

### Step 4: Trigger Deploy
- Look for a **"Trigger deploy"** button (usually top-right)
- Click it to see deployment options
- Select **"Clear cache and deploy site"**
- This will force Netlify to:
  - Clear all cached builds
  - Pull fresh code from GitHub (commit fc2e2d1)
  - Run: `pnpm install && pnpm build`
  - Deploy with fresh _redirects file

### Step 5: Wait for Build to Complete
- Watch the deployment progress
- Should take 2-3 minutes
- Look for green checkmark when complete
- You'll see a message like "Published at: [timestamp]"

### Step 6: Test the Fix
- Go to https://transportvucse.netlify.app
- Should now see the homepage without 404 error
- Try navigating to other routes:
  - https://transportvucse.netlify.app/auth
  - https://transportvucse.netlify.app/dashboard
  - https://transportvucse.netlify.app/landing

## What Gets Fixed
✅ _redirects file (SPA routing)
✅ netlify.toml (proper redirect rules)
✅ next.config.js (cleaned configuration)
✅ All 404 errors should resolve

## If It Still Shows 404 After Redeploy

Check that:
1. Deploy shows "Published" status (green)
2. Build logs show no errors
3. Clear your browser cache (Ctrl+Shift+Delete)
4. Try in an incognito window
5. Check Network tab in DevTools - look for HTML response with 200 status

## Need Help?
- Check Netlify build logs in the deploy details
- Look for any error messages during build
- Verify that both _redirects and netlify.toml are in the repo
