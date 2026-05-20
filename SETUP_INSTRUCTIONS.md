# Wiki Deployment Setup Instructions

This is a separate wiki repository for Outreach Machine documentation.

## Current Status

✅ Wiki files created locally  
✅ Git repository initialized  
⏳ Needs GitHub repository creation  
⏳ Needs Vercel deployment configuration  

## Step-by-Step Setup

### 1. Create GitHub Repository

You have two options:

#### Option A: Using GitHub Web Interface (Recommended)
1. Go to https://github.com/care-consulting
2. Click "New repository" or go to https://github.com/organizations/care-consulting/repositories/new
3. Enter repository name: `outreach-machine-wiki`
4. Description: "Public wiki and documentation for Outreach Machine"
5. Set to **Public**
6. Do NOT initialize with README (we already have one)
7. Click "Create repository"

#### Option B: Using GitHub CLI
```bash
gh repo create care-consulting/outreach-machine-wiki \
  --public \
  --description "Public wiki and documentation for Outreach Machine" \
  --source=/Users/andrea/Documents/outreach-machine-wiki \
  --push \
  --remote=origin
```

### 2. Add Remote and Push (if using Option A)

```bash
cd /Users/andrea/Documents/outreach-machine-wiki

# Add GitHub remote
git remote add origin https://github.com/care-consulting/outreach-machine-wiki.git

# Rename branch to main (if not already)
git branch -M main

# Push to GitHub
git push -u origin main
```

### 3. Create Vercel Project

1. Go to https://vercel.com/dashboard
2. Click "Add New..." → "Project"
3. Import the `care-consulting/outreach-machine-wiki` repository
4. Select project name: `outreach-machine-wiki` (different from main project!)
5. **Framework preset:** Select "Other"
6. **Build Command:** `pip install -r requirements-docs.txt && mkdocs build`
7. **Output Directory:** `site`
8. **Environment Variables:** 
   - PYTHON_VERSION: `3.11`
9. Click "Deploy"

### 4. Configure Custom Domain

Once Vercel deployment is successful:

1. In Vercel project settings:
   - Go to "Domains"
   - Add domain: `docs.care-consulting.it`
   - Copy the provided DNS records

2. Update DNS on SiteGround:
   - Go to SiteGround account
   - DNS Settings for care-consulting.it
   - Update with the Vercel DNS records

### 5. Verify Deployment

- Check Vercel dashboard: Should show successful deployment
- Visit https://docs.care-consulting.it
- Should see the wiki homepage

## Troubleshooting

### If deployment fails with pip errors:

1. Check Vercel build logs for specific error
2. Verify requirements-docs.txt is in root directory
3. Ensure vercel.json is correctly configured
4. Check that Python version is set to 3.11

### If custom domain isn't working:

1. Verify DNS records are correctly added on SiteGround
2. Wait 24 hours for DNS propagation
3. Try accessing via Vercel's default domain first (*.vercel.app)

## Files in This Repository

- `docs/` - All markdown documentation files
- `mkdocs.yml` - MkDocs configuration
- `requirements-docs.txt` - Python dependencies
- `vercel.json` - Vercel build configuration
- `README.md` - Repository overview

## Important Notes

- This is a **separate repository** from the main outreach-machine project
- Do NOT modify the main outreach-machine repository
- All wiki updates should be made here and pushed to GitHub
- Vercel will auto-deploy on every push to main branch

## Next Steps

1. Create the GitHub repository (Step 1)
2. Push the code to GitHub (Step 2)
3. Create the Vercel project (Step 3)
4. Configure the custom domain (Step 4)

Once complete, the wiki will be available at https://docs.care-consulting.it 🎉
