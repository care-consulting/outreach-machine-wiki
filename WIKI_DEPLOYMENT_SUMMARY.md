# Outreach Machine Wiki - Deployment Summary

## Status: ✅ DEPLOYED & INTEGRATED

**Live URL:** https://docs.care-consulting.it

---

## Deployment Details

### Repository
- **GitHub:** https://github.com/care-consulting/outreach-machine-wiki
- **Branch:** main (auto-deploys to Vercel on push)
- **Platform:** Vercel
- **Custom Domain:** docs.care-consulting.it
- **DNS Status:** Valid Configuration ✅

### Technology Stack
- **Generator:** MkDocs with Material theme
- **Language:** Italian (it)
- **Build Command:** `uv pip install --system -r requirements-docs.txt && mkdocs build`
- **Python Version:** 3.11
- **Output Directory:** site/

### Logo
- **Local SVG:** `docs/img/logo.svg` (200x200px, blue background with "OM" text)
- **References:** Updated in mkdocs.yml to use local asset instead of external URL

---

## Integration with Main Application

The wiki is integrated into the Outreach Machine application at **3 locations**:

### 1. Header (Top-Right)
- **Location:** app/page.tsx (line ~121)
- **Element:** "📚 Wiki" link button
- **Position:** Next to Exit button in top-right corner
- **Behavior:** Opens wiki in same window

### 2. Tab Navigation
- **Location:** app/page.tsx (line ~30)
- **Element:** "📚 Wiki" tab in main navigation
- **Position:** Last tab in tab navigation bar
- **Behavior:** Opens wiki in new window

### 3. Footer
- **Location:** app/page.tsx (line ~165)
- **Element:** "📚 Wiki" link
- **Position:** Footer navigation after "Supporto" link
- **Behavior:** Opens wiki in same window

All links point to: `https://docs.care-consulting.it`

---

## Wiki Content Structure

```
docs/
├── index.md                    # Homepage
├── getting-started.md          # First steps (5-30 mins)
├── lead-management.md          # Lead import & organization
├── campaigns.md                # Campaign management
├── email-automation.md         # Email scheduling & personalization
├── analytics.md                # Dashboard & metrics
├── faq.md                      # Frequently asked questions
├── troubleshooting.md          # Common issues & solutions
├── best-practices.md           # Tips & optimization strategies
└── img/
    └── logo.svg               # App logo (local asset)
```

---

## Development Workflow

### To Update the Wiki:

```bash
# 1. Clone repository
git clone https://github.com/care-consulting/outreach-machine-wiki.git
cd outreach-machine-wiki

# 2. Install dependencies
pip install -r requirements-docs.txt

# 3. Edit markdown files
nano docs/lead-management.md

# 4. Test locally
mkdocs serve
# Open http://localhost:8000

# 5. Push to GitHub
git add .
git commit -m "Update guide: [description]"
git push origin main

# 6. Vercel auto-deploys
# Check: https://vercel.com/care-consulting/outreach-machine-wiki
```

---

## Deployment Checklist

- ✅ Repository created on GitHub (care-consulting/outreach-machine-wiki)
- ✅ Vercel project configured
- ✅ Custom domain docs.care-consulting.it working
- ✅ DNS configuration verified
- ✅ Logo fixed (local SVG asset)
- ✅ Build command working (uv pip --system)
- ✅ Wiki links integrated in main app (header, tabs, footer)
- ✅ Documentation updated (README.md, DOCUMENTATION.md, DEVELOPMENT_GUIDE.md)

---

## Monitoring & Maintenance

### Check Deployment Status
- **Vercel Dashboard:** https://vercel.com/care-consulting/outreach-machine-wiki
- **Live Site:** https://docs.care-consulting.it
- **Auto-Deploy:** Enabled (on main branch push)

### Common Issues & Solutions
- **Build fails:** Check requirements-docs.txt and Python 3.11 setting
- **Logo 404:** Ensure docs/img/logo.svg exists locally
- **DNS not working:** Wait 24 hours for propagation, check SiteGround settings

---

## Related Repositories

- **Main Application:** https://github.com/care-consulting/outreach-machine
- **Wiki Repository:** https://github.com/care-consulting/outreach-machine-wiki
- **Live Application:** https://outreach-machine.vercel.app
- **Wiki Documentation:** https://docs.care-consulting.it

---

**Deployment Date:** 20 Maggio 2026  
**Last Updated:** 20 Maggio 2026  
**Status:** Production Ready ✅
