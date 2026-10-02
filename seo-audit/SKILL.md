---
name: seo-audit
description: Audit a website's technical SEO, Google and Yandex search visibility, and evidence-based GEO opportunities. Use for site audits, indexation diagnostics, search traffic analysis, and prioritized SEO findings across projects; not for writing a client proposal or report layout alone.
---

# SEO audit

Use this personal skill for audits of different sites, not as a fixed checklist that every project must pass. Adapt checks to the site's business model, geography, page types, and available access. The output is a defensible diagnosis and prioritized action plan; it is not a promise of indexing, ranking, traffic, or AI citations.

## Scope and inputs

Establish the production domain and mirrors, target markets, business goals, important page types, date/period, audit size, and available owner access. If details are missing, proceed with a clearly bounded public audit and label assumptions. For large sites, report which URL samples or templates were inspected. Do not imply full coverage from a sample.

Choose the applicable level:

- **Public:** inspect reachable pages, code, HTTP responses, robots.txt, sitemaps, and public search results. Do not infer complete indexation or traffic.
- **Owner data:** add Google Search Console, Yandex Webmaster, analytics, logs, or exports only when access exists. Keep each property's domain, permissions, date range, region, device, and source explicit.
- **Strategy:** add demand, competitors, content gaps, links, and commercial priority when the user needs a growth plan and suitable data exists.

For a full audit or an audit-plan/coverage question, read [references/audit-map.md](references/audit-map.md): it contains the complete check map, strategic diagnostics, Google/Yandex procedures, evidence schema, tool candidates, and official-source links. For a narrower technical issue, read [references/technical.md](references/technical.md). For a narrower owner-data, search-performance, or AI-visibility issue, read [references/search-and-geo.md](references/search-and-geo.md). For a narrower strategy, semantic, competitor, local, or backlink question, use the strategic-diagnostics section of the full map. A narrow reference is a quick guide, not a replacement for the full map. Read only the relevant reference(s).

## Working method

1. Inventory important URLs and templates; use a bounded crawl or representative sample. Separate important landing pages from duplicates, parameters, utility pages, and intentional exclusions.
2. Check whether each important page can be discovered, fetched, rendered, indexed, and understood. Compare declared directives with what Google and Yandex actually report when owner data is available. Do not turn a single tool's warning or score into a confirmed finding.
3. Link every finding to evidence: affected URL or template, source and date, observed value, scope checked, expected behavior, and limitation. When a source exposes affected rows, capture or export the URL list before finalizing. Use full absolute URLs in the report and action plan; use path-only examples only inside a clearly labeled sample. Distinguish **confirmed**, **likely**, and **hypothesis**. If access or coverage is missing, state it rather than filling gaps with guesses.
4. Recommend the smallest correction that fits the page's role. For an audit, propose changes; do not silently edit a live site, alter indexing rules, submit sitemaps, change account settings, authorize services, or spend paid credits. Implement fixes only when the user asks for them and permissions are in place.
5. Prioritize by business importance, number of important pages affected, evidence strength, expected impact, and effort. Use P0 for proven crawl/index blocks or critical loss of important pages; P1 for material issues; P2 for local improvements; P3 for investigation or cosmetic work. A long warning list is not an action plan.
6. Recheck important fixes after implementation using the same source and comparable period; search inclusion and AI citations are never guaranteed.

For a full audit, assess release regressions, content performance decline, query/page cannibalization, programmatic-page risks, AI citation-source gaps, and successful AI referral landing pages where relevant data exists. For implementation details and report quality gates, read [references/growth-and-quality.md](references/growth-and-quality.md). SEO/ads overlap applies when paid-channel analysis is in scope. Missing historical snapshots or account data should become a stated limitation or data-collection task.

## Tools and boundaries

Use available structured tools, official APIs, crawler output, and owner exports; no single MCP server is mandatory. Google Search Console MCP, OpenSEO, and GEO Optimizer are optional candidates, not sources of authority. Before using a third-party connector, inspect its provenance, requested scopes, data handling, costs, and relevance to Yandex/CIS markets. Prefer read-only access and property-specific scoping where possible. Never put credentials in the skill or report.

Treat a skill as the method and MCP as access to live data. Search Console has incomplete query rows; third-party rank, backlink, and GEO scores are estimates or samples. Compare platforms separately. Validate time-sensitive rules and tool behavior against current official Google and Yandex documentation when the audit depends on them.

For GEO/AI-visibility audits, treat the core question as: can AI systems safely and confidently use the site's pages as sources for answers? Use [references/search-and-geo.md](references/search-and-geo.md#geo-audit-tasks) for the required GEO task map: AI visibility, GEO query pool, source-page readiness, brand/source citation checks, machine-readable facts, bot access, factual basis, external corroboration, competitor presence, and a GEO action plan.

## Deliverable

Give a handoff-ready audit that another Codex task, SEO specialist, or developer can act on without reopening the search consoles first. Include a short executive summary, a table of findings with evidence and P0-P3 priority, a list of unverified areas, and an ordered implementation/verification plan. Use the complete finding schema in [references/audit-map.md](references/audit-map.md#формат-каждой-находки): ID, block, issue/opportunity, affected URLs/templates, checked count, audit scope, source/date, observation, limitation, confidence, effect, recommendation, priority, and task owner.

For Russian-language audits, write all report headings and subheadings in Russian and use continuous section numbering (`1.`, `1.1.`, `1.2.`). Keep original platform terms such as `Discovered - currently not indexed` only inside evidence cells, status cells, or explanatory text, not as standalone section headings.

In source/status tables, the `Status`/`Статус` column must describe the factual state, not the fact that Codex checked it. Use wording such as `доступен`, `работает нормально`, `данные доступны`, `есть проблемы индексации`, `есть рекомендации`, `ошибка 429`, or `нет доступа`; avoid process labels such as `проверено заново` or `проверено через кабинет`.

For owner-data reporting, use the last 6 months as the default period and provide month-by-month detail for Google Search Console, Yandex Webmaster, Yandex Metrica, GA/analytics, AI visibility, and traffic/conversion tables whenever the source allows it. Include an overall total only in addition to monthly rows, not instead of them. Build equivalent performance tables for both Google and Yandex, using the closest available metrics in each platform. If a UI cannot provide 6-month monthly detail, state the limitation and the exact export/API needed.

The findings table must include a final `Что необходимо сделать` column. Each action cell should be a concrete mini-brief, not a short label like "усилить страницу": specify what to change, which blocks/content/links/technical settings to add or fix, where to verify, and when to request recrawl.

For every count-based finding from a crawl, Google Search Console, Yandex Webmaster, analytics export, log, or third-party tool, add a URL/task appendix. The appendix must include the full URL or exact template, source status/reason, last crawl or metric period when available, business role, concrete correction, expected result, verification step, priority, and owner. If the interface only showed examples or a partial page of rows, label it as a sample and make the first action to export the complete table; do not write as if all affected URLs are known. Prefer attaching/pasting the complete exported list when the finding says "N URLs/pages".

In every URL-level table, make the `Действие` column detailed enough for another Codex branch or implementer to execute. For example: for geo pages include local proof, service area, examples, FAQ, title/description, internal links, CTA, and recrawl; for service pages include service composition, materials, stages, photos, FAQ, portfolio/geo links, CTA, and recrawl; for guide pages include practical blocks, FAQ, links to services/gallery, CTA, snippet improvements, and recrawl. For thin project pages, describe the expected added facts: task, room/type, city/context, materials, complexity, solution, result, alt text, related service/project links, and CTA.

End each full audit with the final section `План задач к действию`. Aggregate the actions from all previous `Действие`/`Что необходимо сделать` columns into one detailed implementation plan with priority, affected URLs/templates, exact work, owner role, readiness criteria, and verification source. This final plan should be directly transferable to a developer, SEO specialist, content specialist, analyst, business owner, or another Codex task.

For each implementation task record the finding IDs, baseline, observable success criterion, failure/reassessment signal, leading indicator, and verification date or event. Separate implementation acceptance from later search/business outcomes. Before delivery, apply the five report quality gates in [references/growth-and-quality.md](references/growth-and-quality.md#контроль-качества-отчета): structure, URL coverage, evidence, executable handoff, and measurements. Resolve unsupported claims or label missing data explicitly; keep the final action plan as the last section.

Keep optional commercial reporting or document styling in a separate reporting workflow.
