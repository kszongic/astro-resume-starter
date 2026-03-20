# Astro Resume Starter

A clean, minimal resume/CV website built with [Astro](https://astro.build). Edit one JSON file, get a beautiful resume with dark mode, print-to-PDF, and perfect SEO.

![Astro](https://img.shields.io/badge/Astro-4-blueviolet) ![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

- **Single JSON config** — Edit `src/data/resume.json` and you're done
- **Dark mode** — Automatic + manual toggle, respects system preference
- **Print to PDF** — Click the PDF button or `Ctrl+P` for a clean printable resume
- **SEO optimized** — Meta tags, semantic HTML, sitemap-ready
- **Responsive** — Looks great on mobile, tablet, and desktop
- **Fast** — Zero JavaScript by default (only tiny theme toggle script)
- **Accessible** — Semantic markup, proper heading hierarchy

## 🚀 Quick Start

```bash
# Clone
git clone https://github.com/kszongic/astro-resume-starter.git
cd astro-resume-starter

# Install
npm install

# Dev
npm run dev

# Build
npm run build
```

## 📝 Customization

1. Edit `src/data/resume.json` with your info
2. Update `astro.config.mjs` with your domain
3. Replace `public/favicon.svg` with your own
4. Deploy anywhere (Vercel, Netlify, Cloudflare Pages)

### Resume JSON Structure

```json
{
  "name": "Your Name",
  "title": "Your Title",
  "email": "you@example.com",
  "website": "https://you.dev",
  "github": "https://github.com/you",
  "linkedin": "https://linkedin.com/in/you",
  "location": "City, Country",
  "summary": "A brief professional summary...",
  "experience": [...],
  "education": [...],
  "skills": { "Category": ["Skill1", "Skill2"] },
  "projects": [...]
}
```

## 🎨 Theming

CSS custom properties in `Layout.astro` control all colors. Modify the `:root` and `.dark` blocks to match your brand.

## 📦 Deploy

Works out of the box on:
- **Vercel**: `npx vercel`
- **Netlify**: `npx netlify deploy`
- **Cloudflare Pages**: Connect repo, build command `npm run build`, output `dist/`

## 📄 License

MIT — use it however you want.
