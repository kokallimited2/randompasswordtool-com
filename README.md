# RandomPasswordTool.com

> **Developer / API / Automation** — Live API Simulator with multi-language code generation.
> Site #5 in the Kokal Operations 12-domain password security portfolio.

---

## 🚀 Deployment

```
randompasswordtool.com → CNAME → kokallimited.github.io/randompasswordtool
```

Push to `main` → GitHub Pages deploys automatically.

---

## ⚠️ SEO Architecture — Individual Blog Post URLs

**This site uses individual HTML files for blog posts, not a modal/JSON approach.**

Each post lives at its own indexable URL:
```
/blog/why-math-random-password-generation.html      ← Google indexes this
/blog/cryptographically-secure-password-api.html
/blog/secrets-management-cicd.html
/blog/password-generation-iam-provisioning.html
/blog/rate-limiting-credential-endpoints.html
/blog/dev-to-prod-secure-password-generation.html
```

`post.json` contains **metadata only** (title, slug, url, excerpt, category, date).
The blog index (`blog.html`) reads post.json and renders cards that **link to** the individual files.

**To add a new post:**
1. Create `/blog/new-post-slug.html` — copy an existing post file as a template
2. Update the `<title>`, `<meta description>`, `<link rel="canonical">`, h1, and article content
3. Update the Article and BreadcrumbList JSON-LD schemas in `<head>`
4. Add a metadata entry to `post.json`
5. Add the URL to `sitemap.xml`
6. Push to `main` — GitHub Actions regenerates sitemap

---

## 📁 File Inventory

| File | Purpose |
|------|---------|
| `index.html` | Homepage + Live API Simulator + Code Generator |
| `blog.html` | Blog index — reads post.json, links to /blog/*.html |
| `blog/*.html` | **6 individual SEO-indexable post files** |
| `contact.html` | Contact form |
| `privacy-policy.html` | UK GDPR + CCPA |
| `affiliate-disclosure.html` | FTC + ASA/CAP |
| `terms.html` | England & Wales |
| `cookie-policy.html` | Cookie table + live preference toggle (key: rpt-ck) |
| `404.html` | Custom 404 |
| `post.json` | Blog metadata only (no full content) |
| `robots.txt` | GPTBot, ClaudeBot, PerplexityBot explicitly allowed |
| `llms.txt` | AI citation guidance |
| `sitemap.xml` | 13 URLs including all /blog/ posts |
| `README.md` | This file |
| `.github/workflows/update-sitemap.yml` | Auto-regenerates sitemap |
| `.github/workflows/validate-html.yml` | Validates required files on PR |

---

## 🔗 Affiliate Slots

Search `AFFILIATE SLOT` in `index.html`:
```
AFFILIATE SLOT 1 — Password manager with CLI (1Password CLI, Bitwarden CLI)
AFFILIATE SLOT 2 — Secrets management (HashiCorp Vault, AWS Secrets Manager)
AFFILIATE SLOT 3 — Identity platform (Okta, Auth0, Ping Identity)
```
All affiliate links require `rel="nofollow sponsored"`.

---

## 🎨 Brand Identity

| Element | Value |
|---------|-------|
| Primary colour | `#22d3ee` (electric cyan) |
| Background | `#0d1117` (GitHub dark charcoal) |
| Accent | `#f97316` (warm orange) |
| Font | JetBrains Mono (display/headers) + Inter (body) |
| Border radius | `4px` (sharpest in portfolio) |
| Header | Cyan **top** border (unique — all others use bottom or none) |
| Cookie key | `rpt-ck` (localStorage) |
| Audience | Developers, DevOps, security engineers |
| Unique tool | Live API Simulator + Code Generator (5 languages, live param updates) |

## Design Differentiation

| | BPG | FSP | IPG | IVK | **RPT** |
|---|---|---|---|---|---|
| Background | Light grey | Warm cream | Near-black | Steel blue | **GitHub charcoal** |
| Primary | Royal blue | Emerald | Electric purple | Iron gold | **Electric cyan** |
| Font | Plus Jakarta Sans | Nunito | Inter | IBM Plex | **JetBrains Mono** |
| Radius | 12px | 18px | 8px | 6px | **4px** |
| Header border | none | bottom-green | none | bottom-gold | **top-cyan** |
| Hero element | Tool | Wizard | Bulk list | Vault badge | **Terminal mockup** |
| Cookie key | bpg-ck | fsp-ck | ipg-ck | ivk-ck | **rpt-ck** |

---

## ✅ SOP Checklist

- [ ] All 15+ files present (15 core + 6 blog posts)
- [ ] 5 schema blocks on index.html
- [ ] Each blog post has its own canonical URL, meta tags, Article schema, breadcrumb schema
- [ ] sitemap.xml includes all /blog/ post URLs
- [ ] post.json — 6 posts, one featured:true, all have `url` field pointing to /blog/slug.html
- [ ] blog.html links to /blog/slug.html (not modal)
- [ ] Code tabs update live with parameter changes
- [ ] robots.txt allows GPTBot, ClaudeBot, PerplexityBot
- [ ] All affiliate links: rel="nofollow sponsored"
- [ ] Cookie key rpt-ck in localStorage
- [ ] GitHub Actions: update-sitemap.yml + validate-html.yml

---

*Operated by Kokal Operations Ltd, United Kingdom.*
