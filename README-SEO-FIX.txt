SANCHORE BAZAAR — GOOGLE INDEXING / REDIRECT FIX

Upload/commit these files to the ROOT of the existing GitHub repository kamlesh9828/sanchore-bazaar (production branch: main). Keep the five HTML files at the repository root.

Files included: index.html, privacy.html, terms.html, refund.html, shipping.html, robots.txt, sitemap.xml.

Changes:
- Policy pages now declare extensionless canonical URLs: /privacy, /terms, /refund, /shipping.
- Homepage policy links point directly to those extensionless URLs.
- Sitemap lists only canonical extensionless policy URLs.
- robots.txt allows crawling and points to the sitemap.
- The original .html files remain in place because Cloudflare Pages Clean URLs uses them to serve the extensionless paths. Do not delete or rename them.

Cloudflare Pages is already configured for automatic deployment from main, so a GitHub commit should trigger deployment. Do not create a second Pages project or add a redirect rule for these same paths.

After deployment, test /privacy, /terms, /refund, /shipping and /sitemap.xml. Then use Google Search Console URL Inspection on each extensionless URL and request indexing. The old .html URLs may continue to appear as redirects while Google refreshes its index.
