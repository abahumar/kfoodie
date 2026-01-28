# KelantanFoodie – MVP Implementation Plan

## Project Overview
KelantanFoodie is a static, fast, SEO-focused local food discovery website built using Astro and deployed on Cloudflare Pages.  
The MVP focuses on **content discovery**, **local SEO**, and **ease of maintenance**, without a traditional CMS.

---

## Objectives (MVP)
- Launch a public, indexable website under kelantanfoodie.com
- Publish 5–10 high-quality Kelantan food blog posts
- Ensure fast loading, mobile-friendly, and SEO-ready
- Keep operating costs close to zero

---

## Tech Stack
- Framework: Astro
- Content: Markdown (file-based)
- Styling: CSS / Tailwind (optional, later)
- Hosting: Cloudflare Pages
- Repository: GitHub
- Analytics: Cloudflare Web Analytics
- Domain: kelantanfoodie.com

---

## Phase 1: Project Setup

### 1. Initialize Astro Project
- Create Astro project using `npm create astro@latest`
- Choose empty project preset
- Use static output mode

### 2. Configure Astro
- Enable MDX / Markdown support
- Ensure `output: static` is set
- Confirm local dev server runs correctly

---

## Phase 2: Content Structure

### Folder Structure

src/
├─ layouts/
│ └─ BlogLayout.astro
├─ pages/
│ ├─ index.astro
│ └─ blog/
│ ├─ index.astro
│ └─ [slug].astro
├─ content/
│ └─ blog/
│ └─ sample-post.md
├─ components/
│ ├─ Header.astro
│ └─ Footer.astro
public/
└─ images/


### Content Rules
- Each blog post is a Markdown file
- Filename = URL slug
- Frontmatter must include:
  - title
  - description
  - pubDate
  - category
  - tags
  - cover image

---

## Phase 3: Blog Implementation

### Blog Listing Page
- `/blog`
- Displays:
  - Title
  - Short description
  - Publish date
- Links to individual blog posts

### Blog Post Page
- `/blog/{slug}`
- Uses `BlogLayout.astro`
- Displays:
  - Title
  - Featured image
  - Publish date
  - Category
  - Content body

---

## Phase 4: Homepage MVP

### Homepage Sections
1. Hero section
   - Clear tagline (Kelantan food focus)
2. Featured categories
   - Nasi Kerabu
   - Street Food
   - Cafe
   - Kuih Tradisional
3. Latest blog posts (3–5)
4. Short About section
5. Footer (contact + social)

---

## Phase 5: Content Creation

### Minimum Content for Launch
- Homepage
- 5–10 blog posts

### Initial Content Focus
- Local intent keywords
- Evergreen Kelantan food topics
- Bahasa Malaysia (primary language)

---

## Phase 6: SEO & Indexing

### On-Page SEO
- Unique `<title>` for each page
- Meta description from frontmatter
- Proper heading structure (H1 → H2)

### Search Engine Setup
- Add site to Google Search Console
- Submit sitemap
- Inspect homepage URL

---

## Phase 7: Deployment

### Cloudflare Pages
- Connect GitHub repository
- Build command: `npm run build`
- Output directory: `dist`
- Enable automatic deployments

### Domain
- Point `kelantanfoodie.com` to Cloudflare Pages
- Enable HTTPS
- Verify DNS propagation

---

## Phase 8: Analytics

- Enable Cloudflare Web Analytics
- Verify page views are tracked
- No cookies required

---

## Phase 9: Testing & Soft Launch

### Pre-Launch Checklist
- Test site on mobile & desktop
- Verify all blog links work
- Check image loading performance
- Confirm no console errors

### Soft Launch
- Share site with small group (friends / WhatsApp)
- Collect feedback on:
  - Readability
  - Page speed
  - Content clarity

---

## Phase 10: Public Launch

- Push final content to main branch
- Trigger Cloudflare deployment
- Submit sitemap again
- Publish first social media post

---

## Post-MVP (Future Enhancements)
- Add Decap CMS for editor-friendly UI
- Add tag & category archive pages
- Improve UI with Tailwind
- Add structured data (Food / Article schema)
- Monetization (featured listings, affiliates)

---

## Success Criteria (First 30 Days)
- Website indexed by Google
- 10–30 daily organic visitors
- At least 1 article ranking for long-tail keyword
- Stable, zero-downtime hosting

---

## Guiding Principle
**Ship early. Improve with data. Avoid overengineering.**