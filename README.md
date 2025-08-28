# Kuna Website

A modern, responsive marketing website for the Kuna iOS app, built for GitHub Pages deployment.

## Overview

This is a static website built with:
- **TailwindCSS** (via CDN) for styling
- **Alpine.js** (via CDN) for interactivity
- **No build process required** - 100% static files
- Mobile-first responsive design
- Dark/light mode toggle
- SEO optimised with structured data

## File Structure

```
website/
├── index.html          # Main landing page
├── privacy.html        # Privacy policy
├── terms.html          # Terms of service
├── robots.txt          # Search engine directives
├── sitemap.xml         # XML sitemap
├── CNAME              # Custom domain configuration
└── assets/
    ├── logo.png        # Main logo (1200x600)
    ├── favicon.png     # Browser favicon
    ├── favicon.svg     # SVG favicon
    ├── apple-touch-icon.png  # iOS icon
    └── screenshots/
        ├── screenshot1.png   # App store screenshots
        ├── screenshot2.png
        ├── screenshot3.png
        └── screenshot4.png
```

## GitHub Pages Deployment

### 1. Create Repository

1. Create a new GitHub repository
2. Upload all files from the `website/` directory to the repository root
3. Ensure the repository is public (required for GitHub Pages on free accounts)

### 2. Enable GitHub Pages

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **"Deploy from a branch"**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**

### 3. Custom Domain Setup (trykuna.app)

1. In your domain registrar's DNS settings, add these records:
   ```
   Type: CNAME
   Name: www
   Value: yourusername.github.io
   
   Type: A
   Name: @
   Values:
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

2. In GitHub Pages settings, enter `trykuna.app` in the **Custom domain** field
3. Enable **"Enforce HTTPS"** once DNS propagates (may take 24-48 hours)

## Content Customisation

### Updating Screenshots

1. Replace files in `assets/screenshots/` with new images
2. Recommended: Use pre-framed iPhone screenshots (current setup)
3. Keep filenames as `screenshot1.png` through `screenshot4.png`

### Changing App Store Links

Update the download links in `index.html`:
```html
<a href="YOUR_APP_STORE_LINK" class="inline-flex items-center...">
```

### Modifying Content

Key sections to customise in `index.html`:
- **Hero section** (lines ~100-140): Main headline and description
- **Features** (lines ~170-250): App features with icons
- **Screenshots** (lines ~280-320): Image carousel
- **FAQ** (lines ~400-500): Frequently asked questions
- **Footer** (lines ~520-550): Contact information

### Updating Privacy Policy

The privacy policy in `privacy.html` uses the official policy from your app documentation. To update:
1. Modify the content in `privacy.html` 
2. Update the "Last updated" date

## Local Development

To test locally:
1. Open `index.html` directly in a web browser
2. All paths are relative, so navigation between pages works locally
3. For a local server: `python3 -m http.server 8000` in the website directory

## SEO Features

- Complete meta tags (Open Graph, Twitter Cards)
- JSON-LD structured data for app information
- XML sitemap for search engines
- robots.txt for crawler directives
- Semantic HTML structure
- Image alt texts and ARIA labels

## Accessibility

- WCAG AA compliant color contrast
- Keyboard navigation support
- Focus indicators on interactive elements
- Semantic HTML structure
- Alt text for all images
- Proper heading hierarchy

## Performance

- CDN-hosted dependencies (TailwindCSS, Alpine.js)
- Optimised images with lazy loading
- Minimal JavaScript footprint
- Fast loading static files

## Branding

- Primary color: `#6C5CE7` (purple)
- Accent color: `#00D1B2` (teal)
- Font: Inter (Google Fonts)
- Logo: Custom Kuna branding

## Support

For website issues, update the repository or contact through the app's support channels.