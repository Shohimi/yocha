# Yocha Legal Documents - GitHub Pages

This folder contains the HTML versions of Yocha's legal documents for deployment to GitHub Pages.

## Deployment Instructions

### Option 1: GitHub Pages (Recommended)

1. **Create a new repository** (or use existing) named `yocha` under your GitHub account
2. **Push this `docs-site` folder** to the repository
3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` (or `master`), folder: `/docs-site` or `/` (if this is root)
   - Save

4. **Your URLs will be**:
   - Privacy: `https://[username].github.io/yocha/privacy.html`
   - Terms: `https://[username].github.io/yocha/terms.html`
   - Index: `https://[username].github.io/yocha/`

5. **Update the URLs in the app**:
   - File: `src/screens/About/index.tsx`
   - Update lines 171 and 178 with your actual GitHub Pages URLs

### Option 2: Custom Domain

If you have a custom domain (e.g., yochaapp.com):

1. Follow GitHub Pages setup above
2. Add a `CNAME` file to this folder with your domain
3. Configure DNS for your domain
4. Update URLs in the app to `https://yochaapp.com/privacy.html`, etc.

### Option 3: Direct GitHub Raw Links (Not Recommended)

You can also use direct GitHub raw links, but they're less user-friendly:
- `https://raw.githubusercontent.com/[username]/[repo]/main/PRIVACY.md`

## Files

- `index.html` - Landing page with links to legal documents
- `privacy.html` - Full Privacy Policy (generated from PRIVACY.md)
- `terms.html` - Full Terms of Service (generated from TERMS.md)

## Testing Locally

To test before deploying:

```bash
# Simple Python server
cd docs-site
python -m http.server 8000

# Then visit http://localhost:8000
```

## Notes

- The HTML files include the full content from PRIVACY.md and TERMS.md
- The styling is mobile-responsive
- All links open in new tabs where appropriate
- Contact email: hello@ninchanese.com
