# Tidewater Invoicing: a dummy site for testing the 27x SEO Agent

Fictional business. Served by GitHub Pages at https://harish-b-213.github.io/ (domain root, so robots.txt,
the sitemap and the agent's GitHub pull requests all work). Plain HTML: each address is one file.

## Deliberate problems (what each agent should find)

| Page | Problem | Expected from the agent |
|---|---|---|
| /pricing.html | Title is 130+ characters | Site Audit: title too long; a title fix as a pull request |
| /contact.html | No meta description; missing from the sitemap | Site Audit: missing description, page not in sitemap |
| /blog/invoice-vs-receipt.html | Same title as /blog/how-to-write-an-invoice.html | Duplicate title; new title as a pull request |
| /blog/ | No H1 (the heading is an H2) | Missing H1 |
| /blog/ and sitemap.xml | Link and sitemap entry for /blog/payment-terms-guide.html, which doesn't exist (404) | Broken link fix; 404 in sitemap |
| /blog/late-payment-reminder-email.html | Image without alt text; published 2022 and never updated | Alt text fix; content refresh idea |
| /features.html | Image without alt text; no SoftwareApplication schema | Alt text fix; schema idea |
| /blog/invoice-template-uk.html | Thin (about 80 words) and competes with /blog/how-to-write-an-invoice.html for "invoice template" | Thin content; merge (consolidate) idea |
| /old-pricing.html | Orphan: no page links to it, but it is in the sitemap | Orphan page |
| /terms.html | `noindex` by mistake | Noindex warning |
| /integrations.html | All content is written by JavaScript | JavaScript-only content (raw HTML has no text) |
| (site) | No /llms.txt | llms.txt proposed as a pull request (A15) |
| /contact.html, /blog/, /404.html | No Open Graph tags on 404; description missing on contact | Low items |

Healthy reference pages: /, /about.html, /blog/how-to-write-an-invoice.html.

## Not covered here
- Search Console and GA4 data need real visits; the site is new, so expect empty Google numbers for a few days.
- Redirects: GitHub Pages can't send 301s.
