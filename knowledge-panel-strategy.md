## 1. Entity building steps
- Publish a canonical About page with an H1 containing exact brand name and a concise verified description.
- Create and maintain an authoritative "Team / Founder" page with bios, structured data (Person schema) and high-quality images.
- Ensure consistent NAP (Name, Address, Phone) across website footer, Contact page, Google Business Profile (GBP), and major directories.

## 2. Schema requirements
- Organization schema on homepage including logo, url, sameAs, contactPoint, and description.
- WebSite + WebPage schemas for About and Contact pages.
- Person schema for founder(s) with sameAs to verified social profiles.
- Breadcrumb schema and FAQ schema where applicable.

## 3. Brand identity consistency signals
- Exact-match business name across GBP, LinkedIn Company Page, website title tags, and About page.
- Use the same brand image assets (logo) across site and social (image hashing consistency).
- Consistent canonical URL, HTTPS, and structured data across site.

## 4. Press & authority signals
- Obtain mentions on reputable domains (local press, industry publications).
- Structured press releases using JSON-LD (NewsArticle) for key announcements.
- Syndicate author bio pages linking back to Workcity site (guest posts with rel=author or rel=publisher where possible).

## 5. About page hierarchy
- URL: `/about` or `/about-us` (canonical)
- H1: exact brand name
- H2: one-line brand descriptor (what you do)
- H3: leadership bios (each with Person schema and sameAs social links)
- H3: press & awards (links to authoritative coverage)
- H3: contact info + local address (for GBP linkage)

## 6. Monitoring & verification
- Claim/verify Google Business Profile.
- Use Google Search Console and Knowledge Graph Search API (if available) to monitor entity signals.
- Use SERP monitoring to track Knowledge Panel changes and authoritative mentions.

