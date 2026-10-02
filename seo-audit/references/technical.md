# Technical SEO checks

Use selectively according to page type and risk. Verify production behavior rather than a local build alone.

## Discovery and server behavior

- Check robots.txt rules for Googlebot and YandexBot, sitemap availability/format, canonical and indexable URLs in sitemaps, important omissions, internal links, orphan candidates, crawl depth, redirects, 4xx/5xx, and broken links. A sitemap does not guarantee indexation. An orphan claim requires a second URL source beyond a link crawl.
- Test missing product and SPA paths. A page that returns 200 with missing/error content may be a soft 404; use meaningful 404/410 or a redirect to a genuine replacement.
- Check HTTPS, selected domain/mirror, consistent internal URLs and redirects. Change existing URL slugs only for a demonstrated issue and with a redirect map.

## Indexability and rendering

- Inspect meta robots and `X-Robots-Tag`, canonical, duplicate/parameter pages, and source versus rendered HTML. A target landing page must not have accidental `noindex`; a utility page may intentionally have one. If robots.txt blocks a URL, the bot may be unable to read its `noindex`.
- Check the published site for `localhost` and preview-domain canonical/links, and preview `noindex` or other build settings leaking into production. Keep preview and production policies distinct.
- Inspect important content, title, canonical, and links before and after JavaScript rendering, including Google URL Inspection and Yandex page/JS-rendering tools when available. CSR alone is not proof of failed indexation. Distinct content on `#/` routes is a discovery risk; prefer real paths and direct entry that resolves correctly.
- Compare CDN/WAF and geographic rules with verified Googlebot/YandexBot requests, URL test results, and server/CDN logs. A WAF being enabled is not itself a defect; a spoofed User-Agent is not proof of bot access. Do not assume Googlebot comes only from the US.

## Content, presentation, and UX

- Review unique, descriptive titles; useful meta descriptions; clear primary heading and logical section headings. Duplicate titles/descriptions are worth clustering by template. Do not flag H1 count or perfect heading order as an automatic Google ranking violation; snippets may be rewritten.
- Check informative-image alt text, image availability, dimensions, formats and compression; decorative images can have empty alt. Check `og:image` for social previews, not as an indexation requirement.
- Validate relevant structured data against visible page facts and search-engine support. Do not demand Schema.org on every page or promise rich results.
- Measure mobile content/navigation and speed on representative templates. Distinguish Google field Core Web Vitals from Lighthouse lab data; Yandex mobile and speed diagnostics are separate sources.

For release regressions, compare saved production snapshots using [growth-and-quality.md](growth-and-quality.md#изменения-seo-после-релизов). Without an earlier snapshot, report only current observations and propose collecting a baseline. Record planned changes separately from accidental losses.

For current implementation rules use official [Google Search Central](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) and [Yandex Webmaster help](https://yandex.ru/support/webmaster/ru/). Recheck specific tool names and directives before reporting them as current.
