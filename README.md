# sonatacx-website — Institutional Website

**Live:** [sonatacx.com.br](https://sonatacx.com.br)

Institutional website for Sonata.cx, a business management and customer experience consultancy. Built as a static site with deliberate choices around performance, SEO architecture, and conversion — no build step, no dependencies, no framework overhead.

---

## Architecture & Design Decisions

### Static-first, by choice

The site runs on plain HTML, Tailwind CSS (CDN), and vanilla JavaScript hosted on Hostinger shared hosting. This wasn't a constraint — it was a decision. Static files load faster, require no server-side rendering, and are trivially cacheable. For a consultancy site whose primary KPI is lead generation, this is the right stack.

### SEO-first structure

Every page was built with organic search in mind from the start:

- **One H1 per page**, always keyword-aligned to commercial intent
- **Unique `<title>` and `<meta description>`** per page, targeting specific search queries (e.g. *"consultoria empresarial para crescimento sustentável"*, *"como avaliar os resultados da empresa no primeiro trimestre"*)
- **`<link rel="canonical">`** on all pages to prevent duplicate content issues
- **Open Graph and Twitter Card meta tags** on every page for consistent social sharing previews
- **Structured data (JSON-LD)** implemented at three levels:
  - `Organization` on the homepage
  - `Article` + `BreadcrumbList` on every blog post
  - `FAQPage` on article pages with Q&A sections to target featured snippets
- **`sitemap.xml`** listing all URLs with `lastmod` and `changefreq`
- **`robots.txt`** with sitemap reference

### Blog as an SEO asset

The blog (`/blog/`) was conceived as a topical authority cluster around the consultancy's core keywords: *gestão empresarial*, *planejamento estratégico*, *customer experience*, *redução de custos*, *melhoria de processos*. Each article:

- Targets a specific search intent (informational + commercial)
- Has an FAQ section designed to capture featured snippet positions
- Contains contextual internal links back to the services section and contact page
- Includes breadcrumb navigation (both visual and JSON-LD) to signal content hierarchy to crawlers
- Shows category, publish date, author and estimated reading time

Articles are written and structured in `.docx` files and converted to HTML via a Python build script that parses paragraph styles, applies Tailwind classes and generates complete, schema-complete pages — no manual HTML authoring required per article.

### Conversion tracking

- Google Analytics 4 (`G-C0J8CEBHSX`) with custom events
- WhatsApp click tracking at all three touchpoints: inline contact link, floating button, and form-to-WhatsApp submission — each with distinct `event_label` for funnel analysis
- Google Ads conversion pixel (`AW-905546952`) fires exclusively after successful lead form submission, not on page load
- Lead capture on the Capacity Planner landing page (`planner.html`) posts to Google Sheets via Sheet.best with no backend required

### Lead gate for tools

The `/planner.html` page acts as a conversion gate for the Sonata CX Capacity Planner (hosted separately on Vercel). Visitors submit name, email, position and company before being redirected — data lands in Google Sheets, GA4 fires a `generate_lead` event, and the Google Ads conversion pixel fires. The tool itself is fully client-side (no data leaves the browser), which is the privacy-by-design pitch on the landing page.

---

## Pages

| Page | Purpose |
|---|---|
| `index.html` | Main institutional page — hero, about, results, services, tools, blog, contact |
| `planner.html` | Lead gate for the Sonata CX Capacity Planner tool |
| `blog/index.html` | Blog listing with category filters, reading time, author |
| `blog/primeiro-trimestre.html` | Article: *Como avaliar os resultados da sua empresa no primeiro trimestre* |
| `blog/vender-mais.html` | Article: *Vender mais não basta: como aumentar o lucro da empresa com mais eficiência* |
| `sitemap.xml` | XML sitemap for all public URLs |
| `robots.txt` | Crawl directives with sitemap reference |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | Tailwind CSS (CDN, JIT) |
| Fonts | Google Fonts — Anta (titles), Raleway (body) |
| Analytics | Google Analytics 4 |
| Ads | Google Ads conversion tracking |
| Lead Capture | Sheet.best → Google Sheets |
| Structured Data | JSON-LD (Organization, Article, BreadcrumbList, FAQPage) |
| Hosting | Hostinger shared hosting |
| Build tooling | Python scripts for article generation and batch updates |

---

## Developer / Portfolio

**Project by: Eduardo Duarte e Araujo**
Role: CX Strategy, Product & AI-Augmented Development

> This repository contains the source code of the institutional website for Sonata.cx, published here for portfolio and code review purposes. The live version is hosted on Hostinger and may differ from the files in this repository.
