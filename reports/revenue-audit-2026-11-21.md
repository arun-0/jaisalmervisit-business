# Revenue evidence — 21 November 2026

This is a dated audit/rollout record, not the current task list or application brief. [Live status/approvals](../TODO.md) · [Strategy](../strategy/roadmap.md) · [Review setup](../setup/revenue-setup.md). Account/private visitor material and raw exports are excluded.

## Account and public checks

| Source / scope | Observed result | Limit |
|---|---|---|
| AdSense site | jaisalmervisit.com Ready; Auto ads and Auto optimise ON; no page exclusions. Preview listed overlay formats 3/3, in-page 1/2, intent-driven 0/1. | Preview/settings do not prove fill or earnings. No account changes saved. |
| AdSense Last 30 days ending 20 Nov, USD | 0 recorded page views, 0 impressions, US$0.00 estimated earnings; RPM unavailable. | AdSense delivery is not total website traffic. Account timezone not independently verified. |
| AdSense Home | Identity Not started; UI said verification required before earning. | Does not alone establish the exact cause of zero delivery. |
| AdSense ads.txt | Not found; last crawled Not applicable; Check for updates still said file not found. | File itself was publicly reachable and correct. |
| HTTP ads.txt/robots | Apex HTTPS 200 with exact publisher seller line; HTTP apex/www reach it. Robots permits public crawling except /admin. Mediapartners-Google user-agent simulation also received 200. | Simulated user agent is not a real Google-IP test. Hosting changed that day; crawler/cache/edge cause not established. |
| Live homepage | Publisher loader present; one slot data-ad-status=unfilled with zero-sized frames. No filled ad observed or clicked. | One visit is not a global fill measurement. |
| Privacy and messaging | European regulations Messages showed onboarding/Create message, not a published message. | Checked code did not establish a third-party certified CMP. Custom analytics notice is not proof of suitable ad consent. |
| Source at production b64961b | Homepage had publisher loader; 35 guides omitted it under empty manual-slot config/length thresholds. Separate Ad Manager provider disabled with empty adUnitPath and its own consent requirement. | Ad Manager is a different integration, not a location for AdSense IDs. |
| Search Console initial session | Business account initially had no accessible property. | Superseded by verified setup below; not evidence of zero search impressions/indexing. |

## GA4 baseline

Property `visitjaisalmer-e3085` / 558450708, **24 Oct–20 Nov 2026**: **176 sessions, 403 views, 43 active users, 41 new users**, average session engagement 2m54s. Landing sessions: `/` 160; `(not set)` 16. The guides launched after this window. Consent-limited collection, internal/test traffic, property timezone and stream/source measurement-ID match were not independently resolved.

Channel totals: Unassigned 121, Direct 36, Organic Social 19; no Organic Search row. Session source/medium detail:

| Source / medium | Sessions |
|---|---:|
| file / (not set) | 37 |
| (direct) / (none) | 36 |
| tourist_companion / (not set) | 35 |
| tts / (not set) | 33 |
| ig / social | 14 |
| list / (not set) | 10 |
| m.facebook.com / referral | 4 |
| reviews / (not set) | 4 |
| voice / (not set) | 2 |
| l.facebook.com / referral | 1 |

Internal names matched UI event origins forwarded as `source`, strongly suggesting attribution pollution. The published adapter change renames that parameter to `interaction_source`; a controlled fresh GA4 check is still required. Historical attribution is not repaired. The fix also honours analytics withdrawal and re-acceptance.

## Published release and verification evidence

| Result | Evidence / meaning |
|---|---|
| Guide/analytics batch | PR 6, main `2939ebb`, Actions [44947673883](https://github.com/arun-0/jaisalmervisit-site/actions/runs/44947673883) passed check/deploy. Four commercial guides improved; guide-click and analytics fixes shipped. Independent guide Auto ads control exists but stays OFF. |
| Ownership file | PR 7, main `c427046`, Actions [44947905108](https://github.com/arun-0/jaisalmervisit-site/actions/runs/44947905108) passed check/deploy. `public/google10227309e0228ef3.html` matched Google's download after the same-origin extensionless redirect; retain it. No DNS/new users/credentials required. |
| Production checks | 35 guides, 37 sitemap URLs and 14 referenced assets passed. Advertising control/consent-order, analytics and delayed/offline/stalled-feed checks passed. Phone-sized browser opened safari contacts, Sam map and provider form; nothing submitted. |
| Sitemap | Property `https://jaisalmervisit.com/` verified; Google confirmed submission. Processing report showed Couldn't fetch/0 discovered with no specific cause. Public XML was 200 application/xml and matched the committed sitemap. Google live test at **20:48 GMT** said URL available/Page can be indexed. Live access is confirmed; processing/indexing is not. |

No affiliate account, paid link, ad-account/CMP activation, operator outreach or identity submission was performed by the audit. Later decisions/status belong in TODO and the worklog trail.

## What the evidence supports

The audience is small and future clean data is needed. Illustrative only: 403 eligible views at US$1–5 incremental page RPM yields about US$0.40–2.02; 100 relevant visits × 10% outbound × 3% completed booking × US$50 commissionable amount × 8% yields US$1.20. These inputs are assumptions except the recorded views and then-advertised rate; neither is a forecast of actual eligibility, attribution or income.

The later [India-first audience assumption](../strategy/roadmap.md#audience-and-market) is not measured country data from this audit.
