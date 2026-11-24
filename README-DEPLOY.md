# Cynthia Chen — Personal Website (Deployment Package)

This folder is a complete, self-contained static website. Upload it as-is to any static hosting service, bind your own domain, and you're live.

## What's Inside

```
index.html          — the entire site (single page)
assets/             — game icons & project screenshots
videos/             — 4 UA creative videos (compressed, 720p, web-ready)
```

## Option A — Netlify Drop (easiest, ~2 minutes)

1. Go to https://app.netlify.com/drop
2. Drag this whole folder into the page
3. Done — you get a URL like `random-name.netlify.app`
4. To use your own domain: Site settings → Domain management → Add custom domain, then follow the DNS instructions (add a CNAME record pointing to your netlify subdomain)

## Option B — Vercel (free, great for custom domains)

1. Go to https://vercel.com/new
2. If you have the folder on GitHub: import the repo. Otherwise use `npx vercel` in this folder from a terminal, or drag the folder in the Vercel dashboard
3. Add your domain: Project → Settings → Domains → add `chenyutong.dev` (or whatever you registered), then point DNS per Vercel's instructions

## Option C — GitHub Pages (free, permanent, needs GitHub account)

1. Create a repo named `<your-github-username>.github.io`
2. Upload all files in this folder to the repo root (including `videos/` and `assets/`)
3. Settings → Pages → Source: deploy from `main` branch
4. Site goes live at `https://<your-github-username>.github.io`
5. Custom domain: Settings → Pages → Custom domain, add your domain and a CNAME record at your registrar

## Option D — Cloudflare Pages (free, best global performance)

1. https://dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets
2. Drag the folder in
3. Custom domains: project → Custom domains → add domain (Cloudflare DNS makes this one-click)

## Notes

- No build step needed — it's plain HTML/CSS/JS. Any static host works.
- Videos are already compressed (~1.7MB each, H.264 + AAC, faststart enabled) — safe to serve directly.
- Suggested domains to check availability: `cynthiachen.dev`, `chenyutong.design`, `cynthia-chen.com`
- Domain registrars: Namecheap (~$10/yr for .com), Cloudflare Registrar (at-cost pricing), or Aliyun/Tencent Cloud if you prefer a Chinese registrar.
