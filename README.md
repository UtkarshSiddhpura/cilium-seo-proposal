# cilium-seo-proposal
`In progress...` as it presents practical approaches for SEO/AIO etc but is not a finished audit. As rn it outlines recommended changes without page-level examples, measured baselines, or a deep codebase/docs review. I still need to inspect most of the codebase, decide and pull imp metrics & Find actual impact making changes I can work on..

## Goals
- Improve organic visibility and impressions.
- Make docs and site answerable by AI assistants (snippets, rich answers).
- Raise click-through rate (better titles/snippets).
- Give contributors clear, practical guidance.

---

## Quick approach
1. Fix technical basics (meta tags, sitemap, robots, performance).
2. Make content scannable and answer-first (TL;DR, clear headings).
3. Add structured data where it helps (FAQ, HowTo, Article).
4. Measure, iterate, scale.

---

## Main site (Gatsby) key tasks
- Ensure each page has a unique title and meta description via Gatsby Head API.
- Add OpenGraph/Twitter tags for social sharing.
- Add JSON-LD where relevant: Article, FAQPage, HowTo, BreadcrumbList.
- Use semantic headings: one H1 per page, clear H2/H3 structure, anchor IDs.
- Improve internal linking and avoid orphan pages.
- Generate sitemap.xml and robots.txt and submit to Search Console.
- Improve performance (images, code-splitting, caching). Run Lighthouse regularly.

---

## Docs site (Sphinx) key tasks
- Use descriptive page titles (top heading becomes `<title>`).
- Add meta descriptions via theme/context or extension for key pages.
- Break content into focused pages (concept pages like `/concepts/kube-proxy-replacement`).
- Start pages/sections with a short TL;DR or definition.
- Use `toctree` and breadcrumbs to ensure everything is reachable.
- Add JSON-LD for FAQs and HowTos where appropriate (via templates or extensions).
- Enable sitemap (e.g., sphinx-sitemap) and verify in Search Console.

---

## Content patterns (what to write)
- Start with a one-sentence answer or TL;DR.
- Use question-like headings for common queries: “What is X?”, “How to do Y?”
- Keep paragraphs short (1–3 sentences). Use bullets and numbered steps.
- Add explicit citations/links for claims, benchmarks, or versioned facts.
- Show author/last-updated metadata on important pages.

---

## Structured data (practical rules)
- Use FAQPage for true FAQs (answers must be on the page).
- Use HowTo for step-by-step guides with clear ordered steps.
- Use Article/BlogPosting for posts (headline, image, author, datePublished).
- Validate with Google Rich Results Test and fix errors reported in Search Console.

---

## Testing & metrics
- Capture baseline: impressions, clicks, CTR, rankings for pilot pages.
- Use Google Search Console + GA4 for organic metrics and indexing issues.
- Use Lighthouse / PageSpeed for performance and Core Web Vitals.
- Manually test AI visibility: query major LLMs for target questions and note citations.
- Track structured data status in Search Console (Enhancements > Rich results).

---


## Contributor checklist
- One clear H1 per page.
- Concise meta description (<155 chars).
- TL;DR or one-sentence answer at top.
- Use H2/H3 to split ideas; add anchor IDs.
- Add internal links to related pages.
- Add FAQ/HowTo schema only when content fully matches schema rules.
- Add author + last-updated on key pages.

---

