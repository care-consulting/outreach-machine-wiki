# Outreach Machine Wiki

Public documentation wiki for Outreach Machine - business user guides.

**Live:** https://docs.care-consulting.it

This is a separate repository dedicated to the Outreach Machine user documentation. It's built with MkDocs and deployed to Vercel.

## Quick Start

### Requirements
- Python 3.11+
- pip

### Setup

```bash
# Install dependencies
pip install -r requirements-docs.txt

# Start development server
mkdocs serve

# Open http://localhost:8000
```

## Building

```bash
# Build static site
mkdocs build

# Output is in the 'site' directory
```

## Deployment

This repository is automatically deployed to Vercel at https://docs.care-consulting.it when you push to main.

### Vercel Configuration
- Build Command: `pip install -r requirements-docs.txt && mkdocs build`
- Output Directory: `site`
- Python Version: 3.11

## Documentation Structure

- **docs/index.md** - Wiki homepage
- **docs/getting-started.md** - Getting started guide
- **docs/lead-management.md** - Lead management guide
- **docs/campaigns.md** - Campaign management
- **docs/email-automation.md** - Email automation guide
- **docs/analytics.md** - Analytics and reporting
- **docs/faq.md** - Frequently asked questions
- **docs/troubleshooting.md** - Troubleshooting guide
- **docs/best-practices.md** - Best practices and tips

## Technology

- **MkDocs** - Static site generator
- **Material Theme** - Modern, responsive documentation theme
- **Vercel** - Deployment platform
- **GitHub** - Version control

## Contributing

To contribute to the documentation:
1. Edit the markdown files in the `docs/` folder
2. Test locally with `mkdocs serve`
3. Commit and push to main
4. Vercel will automatically deploy

## License

Documentation is part of the Outreach Machine project.

---

**Note:** This is a separate repository from the main Outreach Machine application. The main application repository is at https://github.com/care-consulting/outreach-machine.

