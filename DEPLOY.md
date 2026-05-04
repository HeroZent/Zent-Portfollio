# Zent Portfolio — Deploy Bundle

Single-file portfolio site, ready to deploy to any static host.

## Files

```
index.html         ← the entire portfolio (HTML + CSS + JS in one file)
Zent_Resume.pdf    ← linked from the footer "Download Resume ↓"
Zent_Resume.docx   ← optional Word version
vercel.json        ← caching + security headers for Vercel
```

## Deploy to Vercel — 3 ways

### 1. Drag & drop (fastest)
1. Go to https://vercel.com/new
2. Sign in (GitHub / GitLab / Google)
3. Drop this entire folder onto the upload zone
4. Click Deploy
5. Live in ~10 seconds at a `*.vercel.app` URL

### 2. GitHub + Vercel (best for iterating)
```bash
# in this folder
git init
git add .
git commit -m "initial portfolio"
git remote add origin git@github.com:YOURNAME/zent-portfolio.git
git push -u origin main
```
Then on vercel.com → New Project → Import Git Repository → pick the repo.
Every `git push` redeploys.

### 3. Vercel CLI
```bash
npm i -g vercel
vercel        # follow prompts
vercel --prod # promote to production
```

## Custom domain
Once deployed, in the Vercel dashboard go to your project → Settings → Domains → Add. Point your domain's nameservers (or just CNAME) to Vercel's instructions.

## Notes
- No build step needed. Static HTML.
- External fonts and animation libraries (GSAP, Lenis, ScrollTrigger) load from cdnjs — no bundling required.
- The footer "Download Resume" link expects `Zent_Resume.pdf` in the same folder. Already included.
- Total deployed size: ~340 KB (mostly the resume PDF).
