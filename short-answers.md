## 1. Difference between Google Knowledge Graph and Google Knowledge Panel
- Knowledge Graph is Google's internal database of entities and relationships (a knowledge base). It stores facts, relationships, and entity identifiers.
- Knowledge Panel is the public SERP UI that surfaces curated entity information from the Knowledge Graph (the box on the right of desktop results or top on mobile). In short: Graph = database; Panel = the UI.

## 2. How Google determines entity identity
- Google uses multiple signals: structured data (JSON-LD/schema), consistent brand/name mentions across high-authority sites, verified profiles (Google Business Profile, Wikipedia), sameAs links, consistent NAP and canonical URLs, and co-occurrence relationships (how the entity is described across sources). Aggregated, unique identifiers and high-quality corroborating sources cause Google to treat the string as a distinct entity.

## 3. When to create Custom Post Types instead of pages
- Use Custom Post Types (CPTs) when content is repeatable and structured (e.g., Jobs, Events, Case Studies, Team Members) and you need archive pages and taxonomy. Use standard **Pages** for static, hierarchical content (About, Contact, Landing pages). CPTs support custom fields, templates, and better content management.

## 4. Recommended plugins for speed optimization and why
- WP Rocket (paid) — easy critical CSS, caching, minification, lazy loading. Great all-in-one.
- Autoptimize — JS/CSS aggregation and minification (free).
- Perfmatters — script manager, disable unused features, reduce bloat.
- Imagify / ShortPixel — image optimization & WebP generation.
- uery Monitor — identify slow DB queries during debugging.
