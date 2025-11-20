# Vercel Deployment Guide

## Current Issue
Your app builds successfully but may not be displaying due to missing environment variables or runtime errors.

## Steps to Fix

### 1. Add Environment Variables in Vercel
1. Go to your Vercel project dashboard
2. Navigate to **Settings** → **Environment Variables**
3. Add the following variable:
   - **Name:** `GOOGLE_GENAI_API_KEY`
   - **Value:** Your Google AI API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
   - **Environment:** Production, Preview, Development (select all)

### 2. Redeploy Your Application
After adding environment variables:
```bash
git add .
git commit -m "fix: update build script and add vercel config"
git push origin main
```

Or trigger a redeploy from Vercel dashboard:
- Go to **Deployments** tab
- Click the three dots on the latest deployment
- Select **Redeploy**

### 3. Check Vercel Logs
If the page still doesn't load:
1. Go to your Vercel deployment
2. Click on the deployment
3. Check the **Runtime Logs** tab for any errors

### 4. Common Issues

#### Issue: Blank Page
- **Cause:** Missing environment variables
- **Fix:** Add `GOOGLE_GENAI_API_KEY` in Vercel settings

#### Issue: 500 Error
- **Cause:** Runtime error in API routes or components
- **Fix:** Check Runtime Logs in Vercel dashboard

#### Issue: 404 Error
- **Cause:** Incorrect URL or routing issue
- **Fix:** Make sure you're accessing the correct Vercel URL (e.g., `https://your-project.vercel.app`)

### 5. Verify Deployment
Once redeployed, visit:
- Homepage: `https://your-project.vercel.app/`
- Detect page: `https://your-project.vercel.app/detect`
- Tests page: `https://your-project.vercel.app/tests/fruits`

## What Was Changed

1. **package.json**: Removed `NODE_ENV=production` from build script (Next.js sets this automatically)
2. **vercel.json**: Added explicit build configuration
3. **.env.example**: Created template for required environment variables

## Need Help?
If issues persist, share:
- Your Vercel deployment URL
- Runtime logs from Vercel dashboard
- Browser console errors (F12 → Console tab)
