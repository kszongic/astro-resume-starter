# Astro Resume Starter 📄

A clean, minimal resume/CV website built with [Astro](https://astro.build). Edit one JSON file, get a beautiful resume with dark mode, print-to-PDF, and perfect SEO.

[![Astro](https://img.shields.io/badge/Astro-4-blueviolet?logo=astro&logoColor=white)](https://astro.build)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/kszongic/astro-resume-starter?style=social)](https://github.com/kszongic/astro-resume-starter)
[![Deploy to Netlify](https://img.shields.io/badge/deploy-netlify-00C7B7?logo=netlify&logoColor=white)](https://app.netlify.com/start/deploy?repository=https://github.com/kszongic/astro-resume-starter)
[![Deploy with Vercel](https://img.shields.io/badge/deploy-vercel-000?logo=vercel&logoColor=white)](https://vercel.com/new/clone?repository-url=https://github.com/kszongic/astro-resume-starter)

---

## Why This Starter?

Most resume builders lock you into their platform or charge monthly fees. Most "resume templates" are bloated with JavaScript frameworks you don't need for a static page.

This starter gives you:

- **Full ownership** — it's your repo, your site, your data
- **Zero vendor lock-in** — deploy anywhere static sites work
- **Blazing performance** — ships zero JS by default (Lighthouse 100/100)
- **One-file editing** — change `resume.json`, everything updates

## ✨ Features

| Feature | Details |
|---------|---------|
| **Single JSON config** | Edit `src/data/resume.json` — name, experience, education, skills, projects |
| **Dark mode** | Automatic (follows system preference) + manual toggle button |
| **Print to PDF** | `Ctrl+P` or click the PDF button → clean, recruiter-ready output |
| **SEO optimized** | Open Graph tags, semantic HTML, auto-generated sitemap |
| **Responsive** | Mobile-first design that looks great on all screen sizes |
| **Zero JS** | Only a tiny theme toggle script — everything else is pure HTML/CSS |
| **Accessible** | Semantic markup, proper heading hierarchy, ARIA labels |
| **Fast builds** | Astro's static output — builds in under 1 second |

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/kszongic/astro-resume-starter.git
cd astro-resume-starter

# Install dependencies
npm install

# Start dev server (http://localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### One-Click Deploy

| Platform | Button |
|----------|--------|
| **Vercel** | [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/kszongic/astro-resume-starter) |
| **Netlify** | [![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/kszongic/astro-resume-starter) |
| **Cloudflare Pages** | Connect repo → build command: `npm run build` → output: `dist/` |

## 📝 Customization

### 1. Edit Your Resume Data

All your content lives in one file: `src/data/resume.json`

```json
{
  "name": "Jane Developer",
  "title": "Senior Software Engineer",
  "email": "jane@example.com",
  "website": "https://jane.dev",
  "github": "https://github.com/jane",
  "linkedin": "https://linkedin.com/in/jane",
  "location": "San Francisco, CA",
  "summary": "Software engineer with 8+ years of experience building scalable web applications...",
  "experience": [
    {
      "company": "TechCorp",
      "role": "Senior Engineer",
      "period": "2021 - Present",
      "highlights": [
        "Led migration to microservices, reducing deploy time by 60%",
        "Mentored 4 junior engineers through promotion cycles"
      ]
    }
  ],
  "education": [
    {
      "school": "University of California",
      "degree": "B.S. Computer Science",
      "year": "2016"
    }
  ],
  "skills": {
    "Languages": ["TypeScript", "Python", "Go", "Rust"],
    "Frontend": ["React", "Vue", "Astro", "Tailwind CSS"],
    "Backend": ["Node.js", "PostgreSQL", "Redis", "Docker"]
  },
  "projects": [
    {
      "name": "OpenWidget",
      "description": "Open-source embeddable widget framework",
      "url": "https://github.com/jane/openwidget"
    }
  ]
}
```

### 2. Configure Your Site

Update `astro.config.mjs` with your production domain for proper sitemap generation.

### 3. Customize Branding

- Replace `public/favicon.svg` with your own icon
- Modify CSS custom properties in `Layout.astro` to change colors:

```css
:root {
  --color-bg: #ffffff;
  --color-text: #1a1a1a;
  --color-accent: #2563eb;
  --color-muted: #6b7280;
}

.dark {
  --color-bg: #0f172a;
  --color-text: #e2e8f0;
  --color-accent: #60a5fa;
  --color-muted: #94a3b8;
}
```

## 🖨️ Print / PDF Tips

The template includes print-specific CSS for a clean PDF output:

- Headers and footers are hidden
- Colors adjust for print readability
- Page breaks are managed automatically
- Links show their URLs in parentheses

**Pro tip:** Use Chrome's "Save as PDF" for the best results. Set margins to "None" for edge-to-edge printing.

## 📊 Comparison with Alternatives

| Feature | astro-resume-starter | jsonresume.org | reactive-resume | resume.io |
|---------|---------------------|----------------|-----------------|-----------|
| **Free & open source** | ✅ | ✅ | ✅ | ❌ ($) |
| **Self-hosted** | ✅ | ⚠️ (CLI only) | ✅ | ❌ |
| **Zero JS shipped** | ✅ | ❌ | ❌ | ❌ |
| **Dark mode** | ✅ | ❌ | ✅ | ❌ |
| **Print to PDF** | ✅ | ✅ | ✅ | ✅ |
| **One-click deploy** | ✅ | ❌ | ⚠️ (Docker) | N/A |
| **Lighthouse 100** | ✅ | ⚠️ | ❌ | ❌ |
| **Custom domain** | ✅ | ❌ | ✅ | ❌ (paid) |
| **No account needed** | ✅ | ✅ | ✅ | ❌ |

## 🏗️ Project Structure

```
astro-resume-starter/
├── src/
│   ├── data/
│   │   └── resume.json      # ← Your resume content
│   ├── layouts/
│   │   └── Layout.astro      # Base layout + theme CSS
│   └── pages/
│       └── index.astro       # Main resume page
├── public/
│   └── favicon.svg           # Your favicon
├── astro.config.mjs          # Astro configuration
└── package.json
```

## 💡 Tips & Tricks

- **Multiple resumes:** Duplicate `resume.json` and create separate pages for different roles (e.g., `frontend-resume.json`, `backend-resume.json`)
- **Analytics:** Add Plausible or Umami for privacy-friendly tracking — just drop the script tag in `Layout.astro`
- **Custom sections:** Add new fields to `resume.json` and render them in `index.astro` — it's just Astro components
- **Version control your career:** Every edit is a git commit — you get a full history of your career progression

## 🤝 Contributing

Contributions welcome! Feel free to open issues or submit PRs for:

- New sections or layout variations
- Accessibility improvements
- Additional theme presets
- Internationalization (i18n) support

## 📄 License

MIT — use it however you want. No attribution required (but appreciated!).

## Related Projects

- [express-mongoose-starter](https://github.com/kszongic/express-mongoose-starter) — REST API starter with Express + MongoDB
- [bun-websocket-starter](https://github.com/kszongic/bun-websocket-starter) — Real-time WebSocket server with Bun
- [node-background-jobs-starter](https://github.com/kszongic/node-background-jobs-starter) — Background job processing for Node.js
