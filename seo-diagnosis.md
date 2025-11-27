# SEO Diagnosis: Site not indexing after sitemap submission

## 1. Quick checks (first 10 minutes)
- Confirm sitemap URL is added & submitted in Google Search Console (GSC).
- Ensure sitemap returns HTTP 200 and is accessible (open in browser).
- Try `site:yourdomain.com` in Google — any pages showing?

## 2. Crawlability tests
- Use `curl -I https://yourdomain.com` to check HTTP status codes and redirects.
- Ensure no wildcard IP blocks on server or WAF blocking Googlebot.
- Use GSC's "URL Inspection" → "Test live URL" → "Request indexing" for sample pages.

## 3. Robots.txt & noindex audit
- Check `https://yourdomain.com/robots.txt` for Disallow rules blocking the site or sitemap.
- Inspect page source for `<meta name="robots" content="noindex">` or X-Robots-Tag HTTP header.
- Common accidental cause: dev/staging flag left enabled or plugin setting (e.g., "Discourage search engines" in WP).

## 4. Canonical checks
- Check `<link rel="canonical">` on pages — ensure canonical points to the same domain and correct path.
- Beware of cross-domain canonical or trailing slash mismatches causing de-indexing.

## 5. Sitemap structure issues
- Ensure sitemap references canonical URLs only (no 404/500 or disallowed URLs).
- If sitemap >50k entries, ensure index file is used.
- Verify sitemap lastmod dates are reasonable and not future-dated.

## 6. Page speed & indexing blockers
- Very slow pages or timeouts can cause crawl issues. Use Lighthouse/PageSpeed to identify critical JS that blocks rendering.
- Excessive reliance on client-side rendering (SPA) without pre-rendering may prevent Google from indexing content. Use server-side rendering (SSR) or dynamic rendering where needed.

## 7. Search Console debugging steps
- Use "Coverage" report to see indexing errors (Blocked by robots.txt, Server error, Discovered – currently not indexed).
- For "Discovered – currently not indexed" try:
  - Improve internal linking to those pages
  - Submit individual URLs via "URL inspection" → "Request indexing"
- For "Crawl anomaly" check server logs to correlate Googlebot requests with errors.

## 8. Additional checks
- Check for manual actions in GSC (unlikely but important).
- Ensure site is not penalized by spammy backlinks — run a quick backlink profile check.
- Check for duplicate content issues causing de-prioritization.
- Confirm DNS resolution is stable and TTLs are sane.

## 9. Fix & validate
- Fix the identified issues, then:
  - Resubmit sitemap in GSC
  - Use "Request indexing" for priority pages
  - Monitor Coverage & Performance reports daily for 7–14 days

