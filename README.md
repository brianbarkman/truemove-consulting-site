# TrueMove Consulting Website

A professional, enterprise-grade landing site for TrueMove Consulting & Advisory services.

## Quick Start

1. Create a new GitHub repository named `truemove-consulting-site` (or similar)
2. Upload all files from this folder to the repository
3. Enable GitHub Pages in repository Settings → Pages
4. Configure your custom domain

## Files Included

```
├── index.html          # Homepage
├── consulting.html     # Shipper services page
├── advisory.html       # Software advisory page
├── contact.html        # Contact page
├── styles.css          # All styling
├── script.js           # Interactivity & animations
└── README.md           # This file
```

## GitHub Pages Setup

### 1. Create Repository

Go to github.com → New Repository
- Name: `truemove-consulting-site`
- Visibility: Public (required for free GitHub Pages)
- Initialize with README: No (we have our own files)

### 2. Upload Files

Option A - GitHub Web Interface:
- Click "Upload files"
- Drag all files into the upload area
- Commit to main branch

Option B - Git Command Line:
```bash
git init
git add .
git commit -m "Initial site commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/truemove-consulting-site.git
git push -u origin main
```

### 3. Enable GitHub Pages

- Go to repository Settings → Pages
- Source: Deploy from a branch
- Branch: main, folder: / (root)
- Click Save

Your site will be live at: `https://YOUR_USERNAME.github.io/truemove-consulting-site`

### 4. Configure Custom Domain

In Settings → Pages:
- Enter custom domain: `truemoveconsulting.com`
- Check "Enforce HTTPS"

At your domain registrar (GoDaddy, Namecheap, etc.):

**For apex domain (truemoveconsulting.com):**
```
Type: A
Host: @
Values:
  185.199.108.153
  185.199.109.153
  185.199.110.153
  185.199.111.153
```

**For www subdomain:**
```
Type: CNAME
Host: www
Value: YOUR_USERNAME.github.io
```

### 5. Set Up truemoveadvisory.com Redirect

At the registrar where you own truemoveadvisory.com:
- Set up URL forwarding/redirect
- Destination: `https://truemoveconsulting.com/advisory`
- Type: Permanent (301)
- Path forwarding: Off

## Contact Form Setup

The contact form is pre-configured for Formspree. To activate:

1. Go to [formspree.io](https://formspree.io)
2. Create a free account
3. Create a new form
4. Copy your form ID
5. In `contact.html`, replace `YOUR_FORM_ID` with your actual form ID:

```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

Alternative form backends:
- [Netlify Forms](https://www.netlify.com/products/forms/) (if you migrate to Netlify)
- [Basin](https://usebasin.com/)
- [FormSubmit](https://formsubmit.co/)

## Customization

### Colors
Edit CSS variables in `styles.css`:
```css
:root {
    --color-accent: #2c5545;      /* Primary brand green */
    --color-ink: #1a1a1a;         /* Main text color */
    --color-paper: #faf9f7;       /* Background */
}
```

### Fonts
Currently using:
- **Cormorant Garamond** - Display/headings (elegant serif)
- **Outfit** - Body text (modern sans-serif)

To change, update the Google Fonts link in each HTML file's `<head>`.

### Content
All content is in the HTML files. Edit directly:
- Company info, stats, service descriptions
- Contact information
- Page titles and meta descriptions

## Performance Notes

- Pure HTML/CSS/JS (no build step required)
- Minimal JavaScript for smooth animations
- Optimized for Core Web Vitals
- Mobile-responsive design

## SSL/HTTPS

GitHub Pages provides free HTTPS via Let's Encrypt. After configuring your custom domain, check "Enforce HTTPS" in Settings → Pages.

Note: It may take up to 24 hours for the SSL certificate to be provisioned.

## Maintenance

To update the site:
1. Edit files locally
2. Commit and push to GitHub
3. Changes deploy automatically (usually within 1-2 minutes)

---

© 2025 TrueMove Consulting, LLC
