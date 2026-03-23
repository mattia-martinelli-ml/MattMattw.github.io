# Mattia Martinelli — ML Engineering Portfolio

> Professional portfolio showcasing **Machine Learning Engineering**, data pipeline architecture, and aerospace data systems expertise.

![Portfolio Preview](https://img.shields.io/badge/Status-Live-green?style=flat-square)
![Tech Stack](https://img.shields.io/badge/Tech-HTML5+CSS3+Vanilla%20JS-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-black?style=flat-square)

## 🎯 Features

- **Fully Responsive Design** — Mobile-first, optimized for all screen sizes
- **Modern UI/UX** — Glassmorphism effects, smooth animations, dark theme
- **SEO Optimized** — Meta tags, Open Graph, JSON-LD structured data
- **Functional Contact Form** — Integrated with Formspree for email delivery
- **Performance First** — Single HTML file, CSS animations (GPU-accelerated), <50KB total
- **Accessibility** — ARIA labels, semantic HTML, skip links, keyboard navigation
- **Print Friendly** — Professional print CSS for PDF export
- **No Dependencies** — Vanilla HTML, CSS, JavaScript (no build tools required)

## 🚀 Deployment

This portfolio is hosted on **GitHub Pages** and auto-deploys from the `main` branch.

### Local Development

```bash
# Clone the repository
git clone https://github.com/MattMattw/MattMattw.github.io.git
cd MattMattw.github.io

# Open in browser (no server needed)
open index.html
# or
python -m http.server 8000  # Local server
```

### GitHub Pages Auto-Deploy

1. Push changes to `main` branch
2. GitHub automatically builds and deploys
3. Live at: `https://mattmattw.github.io`

## 🎨 Customization Guide

### Update Personal Information

**In `<head>` section:**
- `<title>` — Change page title
- `<meta name="description">` — SEO description
- `og:title`, `og:description` — Social media preview
- JSON-LD Person schema — Update name, email, URLs

**In `<body>` section:**
- Hero section: Update name, tagline, CTA text
- About section: Your background story
- Skills pills: Add/remove technologies
- Projects: Add GitHub repositories and quantified metrics
- Links: LinkedIn, GitHub, email

### Contact Form Setup

Update Formspree ID in the form:
```html
<form id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID">
```

Get your Form ID at: [formspree.io](https://formspree.io)

### Google Analytics Setup

Replace placeholder in `<head>`:
```javascript
gtag('config', 'G-YOUR_ANALYTICS_ID');
```

Get your Analytics ID at: [analytics.google.com](https://analytics.google.com)

### Color Customization

Modify CSS variables in `:root`:
```css
:root {
  --bg: #1a202c;           /* Main background */
  --accent: #3D9BFF;       /* Primary accent (cyan) */
  --gold: #F0C040;         /* Secondary accent */
  --text: #E5E7EB;         /* Text color */
}
```

## 📊 Performance Metrics

- **File Size**: ~45KB (minified, no compression)
- **Load Time**: ~200ms (on 4G)
- **Lighthouse**: 95+ (Performance, SEO, Accessibility)
- **Mobile**: Fully responsive, hamburger menu included

## 📱 Browser Support

- Chrome/Edge: Latest 2 versions
- Firefox: Latest 2 versions
- Safari: Latest 2 versions
- Mobile: iOS Safari, Chrome Mobile

## ♿ Accessibility

- WCAG 2.1 AA compliant
- Semantic HTML5 markup
- Keyboard navigation (Tab, Enter)
- Screen reader friendly
- Skip-to-content links
- ARIA labels on interactive elements

## 📧 Contact Form Features

- Validation (name, email, message required)
- Real-time submission feedback
- Mobile-friendly input fields (16px+ font to prevent zoom)
- Error handling with user-friendly messages
- Spam protection enabled

## 🔧 Tech Stack

```
Frontend:
  ├─ HTML5 (semantic markup)
  ├─ CSS3 (animations, gradients, flexbox/grid)
  └─ Vanilla JavaScript (no frameworks)

Hosting:
  ├─ GitHub Pages (static hosting)
  └─ GitHub Domains (free domain)

3rd-party Integrations:
  ├─ Formspree (contact form)
  ├─ Google Analytics (tracking)
  └─ Google Fonts (typography)
```

## 📧 Updates & Maintenance

### Regular Tasks

- Update projects with new repositories
- Add published papers and articles
- Quarterly content review
- Monitor contact form submissions (Formspree email)

### Version History

- **v2.0** (Current) — Professional audit, SEO, contact form, mobile menu
- **v1.1** — Enhanced animations, new sections (Papers, Portfolio, Certifications)
- **v1.0** — Initial launch with core sections

## 📄 License

MIT License — Feel free to fork and customize!

## 🤝 Contributing

Have suggestions? Found a bug?

1. Create an issue
2. Fork the repository
3. Submit a pull request

## 📞 Get in Touch

- **Email**: martinellimattia@protonmail.com
- **LinkedIn**: [mattia-martinelli](https://www.linkedin.com/in/mattia-martinelli-717088195/)
- **GitHub**: [MattMattw](https://github.com/MattMattw)

---

**Last Updated**: March 2026  
**Maintained by**: Mattia Martinelli
