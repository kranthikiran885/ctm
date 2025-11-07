# Deployment Issues - Root Cause Analysis & Fixes

## 🔴 CRITICAL ISSUE #1: C: Drive is FULL (0 GB Free)

**Impact**: This is blocking ALL builds (local and cloud)

### Immediate Actions:

```powershell
# 1. Delete node_modules (usually 1-2 GB)
cd "d:\Downloads\college-cosmos-home\college-cosmos-home"
Remove-Item -Path node_modules -Recurse -Force

# 2. Delete .next build folder
Remove-Item -Path .next -Recurse -Force

# 3. Clear caches
npm cache clean --force
pnpm store prune

# 4. Delete old downloads/temp files from C:\Users\[username]\Downloads
# Delete C:\Windows\Temp files (if safe)
# Empty Recycle Bin

# 5. Use Disk Cleanup utility:
# Settings > System > Storage > Cleanup recommendations > Clean up recommendations
```

**Expected Result**: Should free 2-5 GB of space

---

## 🔴 CRITICAL ISSUE #2: Render Backend Configuration Wrong

**Current Problem**:
- Render is treating backend like a static site
- Looking for "publish directory" which doesn't exist for Node.js apps
- Build command is `pnpm install` (incomplete)

### Fix: Render Backend Configuration

**Go to Render Dashboard for your backend service:**

1. **Settings** → **Build & Deploy**
2. Set these values:
   - **Build Command**: `pnpm install`
   - **Start Command**: `node backend/server.js`
   - **Root Directory**: (leave blank or set to `/`)
3. **DO NOT SET** "Publish directory"

**Alternative: Use render.yaml** (Already in your repo)

Create/Update `render.yaml` in repository root:

```yaml
services:
  - type: web
    name: ctms-backend
    env: node
    plan: free
    buildCommand: pnpm install
    startCommand: node backend/server.js
    rootDir: .
    envVars:
      - key: MONGODB_URI
        value: mongodb+srv://kranthi:kranthi%401234@cluster0.ycbgnbj.mongodb.net/?appName=Cluster0
      - key: JWT_SECRET
        value: ctms_super_secret_jwt_key_for_development_only_change_in_production
      - key: PORT
        value: 5000
      - key: NODE_ENV
        value: production
      - key: FRONTEND_URL
        value: https://your-netlify-domain.netlify.app
```

---

## 🟡 ISSUE #3: Netlify Frontend (Secondary - will work once space freed)

**Current Status**: netlify.toml is correct in repo root
- Base: `college-cosmos-home/`
- Publish: `.next`
- Command: `pnpm install && pnpm build`

**Will deploy successfully once C: drive has space**

---

## Step-by-Step Recovery Plan

### Phase 1: Free Disk Space (NOW - Do this first!)
1. Delete node_modules from local project
2. Delete .next folder
3. Clear package manager caches
4. Delete temporary files from C:\

### Phase 2: Fix Backend on Render
1. Go to Render dashboard
2. Update backend service settings (or use render.yaml)
3. Set correct build/start commands
4. Redeploy

### Phase 3: Test and Deploy Frontend
1. After space freed, reinstall: `pnpm install`
2. Build locally: `pnpm build`
3. If successful, trigger Netlify "Clear cache and deploy"

---

## Key Files Already in Repo
- ✅ `netlify.toml` - Correct configuration for frontend
- ✅ `render.yaml` - Correct configuration for backend
- ✅ All code fixes applied
- ✅ netlify.toml in repo root

Everything is ready once disk space is freed!
