# Revenue audit and next actions — 21 November 2026

## Rollout update — owner-approved publication and Search Console

The owner approved the tested release and Search Console setup in chat. PR 6 is merged; main 2939ebb and Actions run 44947673883 published the commercial guide and analytics changes successfully. PR 7/main c427046 and successful run 44947905108 add Google's ownership file. Both deployed releases passed checks for all 35 guides, 37 sitemap URLs and 14 assets. Guide Auto ads remains OFF.

The business account now owns the verified URL-prefix property https://jaisalmervisit.com/. HTML file verification succeeded; retain public/google10227309e0228ef3.html in future builds. No DNS, credential or user-access change was required. The earlier access gap below is historical.

Google confirmed sitemap submission, then initially reported Couldn't fetch with no specific cause. The public 200 application/xml response matches the committed sitemap. Search Console’s live URL test of the sitemap at 20:48 GMT returned “URL is available to Google” and “Page can be indexed”. This confirms a real Google live fetch, rather than only a simulated user agent. The Sitemaps table still showed Couldn’t fetch on revisiting; performance/indexing reports are also processing. Sitemap processing remains unresolved and should be checked after Google updates it, without repeatedly resubmitting unchanged XML. No indexing request was made for the XML file. Do not describe the sitemap as successfully processed or its URLs as indexed until Google reports that.

[Search Console property](https://search.google.com/search-console?resource_id=https%3A%2F%2Fjaisalmervisit.com%2F) · [Sitemaps](https://search.google.com/search-console/sitemaps?resource_id=https%3A%2F%2Fjaisalmervisit.com%2F)

## Owner update and current work order

On 21 November the owner confirmed AdSense identity verification is Not started and plans to involve a cousin on 22 November. The owner requested explanations before deciding on Viator and personalised ads. Neither is an approval to enrol, accept terms or change ad settings. Read [the affiliate explanation](../explanations/affiliate-pilot-explanation.md) and [the advertising/consent explanation](../explanations/advertising-consent-explanation.md).

The authoritative live todo order is now [the roadmap priority queue](../strategy/roadmap.md#current-priority-todo-list). The initial opportunity table below preserves the audit's earlier decision context; completed site/Search Console work must not be treated as pending setup.

## Recommendation

Fix the account obstacles, create a working search-discovery route and launch one self-service affiliate route. The current measured audience is small: optimise for a few completed bookings and qualified visits, rather than spending heavily on ad layout experiments or a booking backend. The owner asked us to prepare the affiliate route; no existing approved programme or paid referral agreement has been supplied.

The accompanying site branch improves the Sam, Khuri, camel-safari and jeep-safari guides, adds internal enquiry links and guide-click events, corrects analytics consent handling and isolates internal UI sources from acquisition attribution. These four pages were selected for purchase intent and weak existing answers, not measured guide demand. All 35 guides were launched on 21 November, after the baseline window below. No affiliate commission or booking capability is claimed by these changes.

## Observed evidence

Read-only inspection used the existing signed-in business Chrome session. Only aggregate findings are recorded here; IDs, identity documents, banking details, visitor data and account exports are not stored.

| Source | Window / scope | Finding | Limit |
|---|---|---|---|
| AdSense publisher pub-9028150722368329 | Site and account checked 21 November | jaisalmervisit.com is Ready; Auto ads ON, Auto optimise ON; no page exclusions. Preview lists overlay formats 3/3, in-page formats 1/2, intent-driven 0/1. | Settings and ad previews do not prove actual delivery. No ad settings were saved. |
| AdSense Reports | Last 30 days preset, ending 20 November; USD | 0 recorded page views, 0 impressions, US$0.00 estimated earnings; page/impression RPM unavailable. Home also showed US$0.00 this month. | This is AdSense delivery data, not total website traffic. Account reporting timezone was not independently verified. |
| AdSense Home | 21 November | Identity verification Not started; UI says verification is required before earning. | Payee/payments administrator must complete privately. The exact cause of zero delivery is not established by this notice alone. |
| AdSense ads.txt | 21 November | Not found; last crawled Not applicable; Check for updates returned Couldn't find an ads.txt file. | The recheck did not resolve the warning. It does not establish a malformed file. |
| Public HTTP checks | 21 November | HTTPS apex ads.txt returns 200 and Google's exact required seller line; HTTP apex and HTTPS www reach the same file; robots.txt permits crawling except /admin. Mediapartners-Google user agent also received 200. | A user-agent simulation is not proof that Google's real crawler/IP was allowed. Hosting moved today; Google crawl/cache lag or edge access remains possible. |
| AdSense Privacy and messaging | European regulations Messages tab, 21 November | Onboarding/Create a European regulations message; no published message shown. | No evidence of a third-party certified CMP was found in the checked site code. The existing custom analytics notice is not proof of advertising consent. |
| Live browser ad check | 21 November, one fresh homepage visit | Publisher loader present; one AdSense slot reported data-ad-status=unfilled with zero-sized advertisement frames. No filled ad was observed and no ad was clicked. | One client/visit cannot establish global fill; corroborates the zero historical delivery report. |
| Site source | Current production b64961b | Homepage has AdSense loader; all 35 guides omit it. Empty manual slots and article thresholds also suppress the loader. Separate Ad Manager provider is disabled, has an empty adUnitPath and requires JM_CONSENT.ads. | Ad Manager is a different integration; do not insert AdSense unit IDs there. |
| GA4 | visitjaisalmer-e3085, property 558450708; 24 Oct–20 Nov 2026 | 176 sessions, 403 views, 43 active users; 41 new users; average session engagement 2m54s. Landing pages: / 160 sessions; (not set) 16. | Consent-limited observed traffic; internal testing not excluded/verified. Property timezone and stream ID were not independently checked against the source measurement ID. No recorded guide landings in this pre-launch window. |
| GA4 acquisition | Same 28 days | Unassigned 121, Direct 36, Organic Social 19; no Organic Search row. | Attribution is suspect: see source breakdown and code finding below. This does not prove Google has indexed no pages. |
| Search Console | Signed-in business account, 21 November | Welcome/Add a website; no accessible property or performance/sitemap report. | Another account may hold a property. Do not describe this as zero impressions or confirmed de-indexing. |
| Public directory | Preview using production public feed, 21 November | Camel safari deep link opens an activity sheet with local operator contact options. Map and directory checks are recorded in WORKLOG. | Contacts have no supplied paid referral terms. An enquiry is not a booking; do not contact operators without approval. |

GA4 Session source/medium rows (all 176 sessions): file / (not set) 37; (direct) / (none) 36; tourist_companion / (not set) 35; tts / (not set) 33; ig / social 14; list / (not set) 10; m.facebook.com / referral 4; reviews / (not set) 4; voice / (not set) 2; l.facebook.com / referral 1.

Internal names matching code event origins are strong evidence of attribution pollution. The analytics adapter forwarded its internal `source` field unchanged. The patch forwards that field as `interaction_source`. This is a preventative fix supported by the dashboard/code match; a controlled GA4 verification after publication is still needed to confirm the historical cause. Historical data will not be repaired. It also stops forwarding after analytics consent withdrawal and correctly re-grants consent when visitors accept again.

## Ranked opportunity queue at the initial audit

Effort figures below are planning estimates, not limits or promises. Rankings can change with owner feedback and results.

| Priority | Action and revenue mechanism | Expected return / confidence | Setup and recurring work | Next decision |
|---|---|---|---|---|
| 1 | Owner completes AdSense identity verification; recheck account delivery and ads.txt after Google refreshes. | Necessary account hygiene, zero current delivery. Absolute ad upside likely small at current measured scale. High confidence in notices, unknown contribution to fill. | Owner documents/submission, then Google's review. Engineering follow-up roughly 20–45 min if notices clear; more if crawler access remains faulty. | Owner privately submits verification; report status only. Avoid repeatedly changing the correct ads.txt or weakening edge security without evidence. |
| 2 | Establish Search Console access for the named site, verify ownership and submit the existing 37-URL sitemap. Diagnose actual indexing/query demand before expanding content. | Search can create purchase-intent visits; current access gap prevents diagnosis. No uplift promised. | Roughly 20–45 min if existing ownership verification works; inspect resulting coverage as data arrives. | Approve adding the URL-prefix property https://jaisalmervisit.com/ under the business account, or supply access to an existing property. DNS changes require a separate concrete approval if necessary. |
| 3 | Apply to Viator affiliate programme, then add approved, disclosed links to matching safari/itinerary pages. | 8% advertised commission and 30-day window; commission after experience completion. Current account acceptance, attribution and realised outcomes unverified. | Owner legal/payee details and terms; roughly 30–60 min for engineering link integration after approval. Ongoing inventory/link review and monthly payout reconciliation; no owner booking desk. | Owner approves programme/application and personally accepts terms. Use generated partner links, not invented affiliate IDs. |
| 4 | Publish the prepared commercial guide and analytics fixes. | Better answers and paths into existing enquiries; future affiliate placement. No immediate paid-referral mechanism. High confidence in technical changes, demand/conversion effect unknown. | Implemented and tested; review/publish remains. Check qualified clicks and bookings as they mature. | Approve the concrete site release after preview review. |
| 5 | Publish a reviewed Google European regulations message; expand eligible guide AdSense coverage with the prepared independent loader control. | Restores a missing integration only when the account/content/consent setup supports serving. Do not pad guides for ads. | CMP review plus integration/region verification. No reason to create manual units or paid tooling yet. | Review message/site/privacy choices and eligible content before enabling. Auto ads remains OFF in the guide build; existing account settings unchanged. |
| Later | Paid directory placement or direct referrals with a current operator; targeted social acquisition. | Can beat affiliates if an operator pays and fulfils reliably. No current commercial terms supplied. | Sales, collection, cancellations and lead reconciliation must be priced into owner time. | Draft a specific partner offer only when its expected return beats the self-service route. No outbound messages sent. |

## Revenue sensitivity, not a forecast

- At the observed 403 views, an illustrative incremental US$1–5 page RPM implies US$0.40–2.02 per comparable window if every view were eligible. Actual incremental guide views, fill, RPM and consent eligibility are unknown. This does not estimate total traffic from consent-limited GA4.
- At 100 relevant visits × 10% outbound clicks × 3% completed booking conversion × US$50 commissionable order × 8%, affiliate commission is US$1.20. All inputs except the advertised commission rate are illustrative. Three completed US$50 commissionable orders produce US$12 before operating costs, subject to programme rules.
- Content and acquisition have to increase qualified visits for material revenue. No large passive-income claim is supported by the baseline.

## Affiliate pilot prepared for review

Recommend [Viator](https://partnerresources.viator.com/) first because a simple tracked link can test Jaisalmer activity demand without operating customer support or building an API integration. The programme advertises 8% on bookings within 30 days and commission after completion; bank-transfer payout has a US$50 threshold. Confirm the offered contract, eligible commission base, payout route and tax requirements in the actual application. [Programme mechanics](https://partnerresources.viator.com/travel-content/)

Inventory candidates checked on 21 November, not endorsed or date-availability checked:

| Visitor intent | Candidate | Editorial check before linking |
|---|---|---|
| Sunset excursion without an overnight stay | [Half-Day Sunset Camel Safari, product 178630P1](https://www.viator.com/tours/Jaisalmer/Half-Day-Sunset-Camel-Safari/d24761-178630P1) | Confirm route, pickup, actual riding time, inclusions and cancellation terms on the live date. Do not describe it as a Khuri or Sam camp unless the product says so. |
| Open-air overnight safari | [Overnight Non-touristic Camel Safari, product 245696P1](https://www.viator.com/tours/Jaisalmer/An-Overnight-Non-touristic-Camel-Safari-2PM-to-11-30-AM-Next-Day/d24761-245696P1) | The listing describes open-air sleeping and no tents/washroom. It is not a luxury camp. Make this distinction prominent. |

Do not copy ratings or live prices into static copy. Use programme-generated product links with a separate sub-ID per placement, for example `camel-guide-sunset` and `desert-itinerary-overnight`, using whatever tracking field the approved programme supports. Add `rel="sponsored noopener"` and a nearby disclosure: “We may earn a commission if you book through these links. Check current prices, inclusions and cancellation terms on Viator.”

GetYourGuide is a fallback if its approved account or particular inventory is stronger. Its [programme](https://partner.getyourguide.support/hc/en-us/articles/13981068165917-Our-partner-program) also supports tracked links and post-activity commission; [payment guidance](https://partner.getyourguide.support/hc/en-us/articles/14585977727645-Payment-101-threshold-payment-details-proof-of-transaction-and-reports) describes an 8% base and bank threshold. Avoid running two programmes merely to create options at this traffic level.

Before account submission, the owner supplies legal payee/account type, business site, contact and country, intended promotion method and the payment/tax information requested by the programme, privately. Do not infer these from the domain or publish them in Git. No affiliate account was created and no terms accepted in this session.

### Application draft

Use the following only where the actual application asks for a site description or promotion plan. The owner supplies legal identity, country, contact, tax and payment fields directly to the programme and reviews its current terms. Acceptance and availability in the owner's country have not been verified.

> Jaisalmer Visit is an independent English-language travel guide and local provider directory at https://jaisalmervisit.com. We publish destination guides, itineraries and activity-planning information. We plan to place clearly disclosed, contextual affiliate links in relevant Jaisalmer safari and itinerary guides, directing visitors to matching experiences on Viator. Visitors would complete reservations and payment on the booking platform. We will not collect booking payments or imply that an enquiry confirms a reservation.

If asked for audience size, give the measured period and limitations: 43 active users, 176 sessions and 403 views in GA4 for 24 October–20 November 2026; consent-limited measurement, internal testing not verified/excluded. Do not substitute targets for actual traffic. No application has been submitted.

| Setup item | Current revenue unit |
|---|---|
| Chat | Same chat for review, approval, release and acceptance checks; avoid copying account evidence into a new chat. |
| App | Local Codex for repository work; owner uses signed-in Chrome for private identity/application submissions. |
| Project | Jaisalmer Visit, C:\dev\ai\ghanu-jaisalmer-visit; site and business are separate sibling repositories. |
| Model | GPT-6.2 Sol, Medium for implementation and evidence reconciliation; a practical recommendation, not a measured cost optimum. Manual document submission needs no model. |
| Exact prompt | “Continue from business/reports/revenue-audit-2026-11-21.md and the newest WORKLOG entry. Apply only my stated approvals, verify the resulting release/account state and update both records.” |
| Follow-up and stop | Approve/revise site PR 6; approve/defer Search Console setup; provide identity status and programme approval/links. Stop before unapproved production/account changes, new access grants, legal acceptance or private document submission. Continue independent authorised work. |

## Proposed ad/consent rollout

Google's [European regulations guidance](https://support.google.com/adsense/answer/13554116?hl=en-GB) and [non-personalised ads guidance](https://support.google.com/adsense/answer/9007336) explain why the existing “non-personalised” wording and denied Consent Mode defaults alone do not establish a suitable regional advertising consent setup.

Prepare a Google CMP message for jaisalmervisit.com only, English, linking the existing /privacy policy, with consent, refusal and manage-options choices. Keep analytics as the existing separate opt-in during the initial ad rollout; do not silently enable advertising consent-mode integration or other account-wide options. Review the generated message, ad partners, privacy wording, regional behaviour and compatibility with the custom notice before publication. No message or privacy/account setting has been changed.

The site now supports `auto_ads` separately from manual slots and article length. It remains false. The account's existing overlay settings include all three overlay formats; their utility-page impact also needs review before broader coverage. A loader/network request is not a filled impression. Verify a real non-self-clicked ad response and reporting after activation; never click live ads to test revenue.

## Measurement and review

Record guide_action_click, consented provider-contact events and affiliate outbound clicks separately from completed experiences, net commission, cancellations and money received. Existing provider enquiries have no agreed commission. Create custom GA4 dimensions only if needed to inspect guide_path/destination_path/action/interaction_source; their registration is a separate account change. Standard event totals remain usable without those dimensions.

Review early technical delivery as soon as activation changes settle. Compare traffic, completed bookings and commission after approximately 14–28 days from the actual production/affiliate launch, extending when outcomes have not matured. Keep improving the highest-return actions in the same revenue work unit; no automatic stop at a date or page count. Automate link checks/reconciliation when repeated manual work justifies it. No recurring automation was scheduled.

## Validation and publication record

- Site branch: revenue/desert-conversion-and-ad-readiness; commit 75c628f.
- Preview: https://a0f36b6a.jaisalmervisit.pages.dev (review alias https://review.jaisalmervisit.pages.dev).
- Static release checks pass locally and against the preview: 35 guides, 37 sitemap URLs and 14 referenced assets.
- Regression checks pass for Auto ads/manual-slot independence, consent-default ordering, analytics withdrawal/re-acceptance and UI source isolation. Existing delayed/offline/stalled public-feed checks pass.
- Mobile browser check at 390×844: no horizontal overflow; safari deep link opened live local contact options, Sam map opened its location popup, and Add Your Service opened the form without submission.
- Branch CI succeeded: https://github.com/arun-0/jaisalmervisit-site/actions/runs/44946521402.
- Site review: https://github.com/arun-0/jaisalmervisit-site/pull/6 (merged after explicit owner approval).
- The initially reviewed batch was published after explicit owner approval; see the rollout update above. No paid affiliate link, ad-account setting, operator contact, DNS change or identity submission has been made.
