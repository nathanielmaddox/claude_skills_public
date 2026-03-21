# SEO & Content

Skills for search engine optimization and content strategy. Designed to pass Semrush, Google Search Console, AND Ahrefs audits simultaneously.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| SEO Content Strategist | `seo-content-strategist` | Keyword research, content optimization, E-E-A-T, thin/duplicate content, GEO/AEO |
| SEO Link Builder | `seo-link-builder` | Digital PR, outreach, backlink acquisition (Skyscraper Technique) |
| SEO Technical Specialist | `seo-technical-specialist` | Core Web Vitals, crawlability, indexing, structured data, cross-tool audit |

## When to Use

- **seo-content-strategist** -- Content planning, keyword strategy, on-page SEO, thin content fixes, template page differentiation
- **seo-link-builder** -- Link building campaigns, digital PR, backlink strategy
- **seo-technical-specialist** -- Site speed, crawl errors, schema markup, indexing issues, canonical/sitemap, OG/Twitter, heading hierarchy

## Cross-Tool Full Audit (Recommended)

For a comprehensive audit that passes all three tools (Semrush + GSC + Ahrefs), use both SEO skills in a two-wave approach:

**Wave 1 (5 parallel agents):** Meta titles/descriptions, structured data/schema, heading hierarchy/alt text, canonical/sitemap, OG/Twitter cards

**Wave 2 (5 parallel agents):** Thin/duplicate content, technical flags (404 page, trailing slashes, viewport, lang, rel attrs), schema strict validation, internal linking/orphan pages, Core Web Vitals hints

## Key Flags by Tool

| Tool | Unique Flags It Catches |
|------|------------------------|
| **Semrush** | Duplicate titles/descriptions, thin content, missing H1, OG issues, orphan pages |
| **Google Search Console** | Mobile usability, Core Web Vitals (CLS/LCP/INP), structured data errors, index coverage |
| **Ahrefs** | Orphan pages, link depth >3, noindex+sitemap conflicts, duplicate content, broken links |

## Usage Examples

```
Skill({ skill: 'seo-content-strategist', args: 'Fix thin content on template-generated pages' })
Skill({ skill: 'seo-link-builder', args: 'Plan a backlink campaign for otesse.com launch' })
Skill({ skill: 'seo-technical-specialist', args: 'Full cross-tool audit of otesse-app' })
```
