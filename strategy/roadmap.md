# Jaisalmer Visit revenue plan

Updated 21 November 2026 after the owner chose an 80/20 phase focused on revenue with little recurring work. Firebase billing is handled, as confirmed by the owner.

## Current phase

The objective is additional net revenue from the existing site and audience, with a small amount of owner time. Rank opportunities by credible monthly revenue after direct costs, setup effort, ongoing owner minutes and confidence in the evidence. These estimates guide a decision. Actual revenue will establish the winner.

Use the existing website, directory and accounts. The initial operating assumption is a maximum of three small changes and about 15 minutes of owner review per week after setup. Record the owner time needed for approvals, local facts and partner administration separately from engineering time. Adjust that assumption with the owner if an otherwise attractive opportunity needs more time.

The first business commit, `f68e2a5`, already identified the core opportunities. Crawlable pages, ad monetisation, affiliate links and directory income remain useful parts of that plan. The current phase changes their sequence and the amount of recurring work.

## Already delivered

The site and business materials have separate private repositories. The live Cloudflare release includes 35 concise guides, homepage links, unique metadata and a 37-URL sitemap. The partner list renders each eligible business once, attraction photos have descriptions, and slower first visits load published directory data. Search indexing, ad fill and earnings still need account evidence. [Release worklog](../WORKLOG.md)

A code check on 21 November found the AdSense publisher loader in the homepage. It is absent from all 35 generated guide pages. The guide builder emits it only when manual slots are configured and the article meets the builder's length threshold. The current slot list is empty. This is the first monetisation candidate to inspect. It does not establish the value of those guide visits or the site's current ad approval.

## The three candidates, in provisional order

| Candidate | Smallest useful action | Evidence and owner effort | Decision |
|---|---|---|---|
| Recover earnings from existing ad-eligible visits | Inspect AdSense approval, actual delivery, page traffic, exclusions and the guide-template loader. Prepare the smallest suitable integration for eligible guides. Assess Auto ads and one controlled experiment if the account and content support them. | Existing account access, current settings and a recent complete reporting window. Engineering should handle integration and verification. The owner approves the concrete ad setting or publication. | Ship a demonstrated missing integration or test one supported setting. Compare total earnings, page RPM and usability. Low traffic means the absolute upside may be small. [Google setup](https://support.google.com/adsense/answer/9261307) · [Auto ads experiments](https://support.google.com/adsense/answer/9726342) |
| Add a booking path on the pages closest to a purchase | Select one approved affiliate programme or an existing partner with agreed terms. Put a relevant booking link on at most three existing pages where visitor intent and bookable inventory match. Use clear commercial disclosure and link-level tracking. | Confirm programme access, current Jaisalmer inventory, attribution, commission, cancellations and who handles the booking. Prefer traveller self-service and supplier fulfilment when available. | Use completed bookings and realised commission as the outcome. A commission is contingent on the programme's rules and the activity taking place. Affiliate links were already in the seed plan. [Programme mechanics example](https://partner.getyourguide.support/hc/en-us/articles/13981068165917-Our-partner-program) |
| Improve the few pages with the best revenue opportunity | Use available search and landing-page data to choose up to three existing pages. Improve a weak title, missing answer, internal link or relevant booking action. Check sitemap submission and coverage once. | Recent queries, page visits and a short local fact check where needed. Page selection follows evidence. Sam, Khuri, camps, safaris and itineraries are candidates until their demand is measured. | Measure qualified visits and earnings from those pages. Expand only after seeing demand or a specific fix worth making. Sitemap submission helps discovery and cannot guarantee indexing. [Google Search Central](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview) |

This order is provisional. If AdSense is healthy and there is strong purchase intent, the booking path may be the best first change. If an existing operator is already willing to pay for a clearly labelled placement and can fulfil the service, compare that opportunity with the affiliate option. Record the sales, collection and support time before choosing.

A direct referral pilot belongs in this phase only when an existing relationship, agreed terms, attribution and supplier fulfilment make it inexpensive to operate. An owner-run WhatsApp booking desk brings response, availability, cancellation and reconciliation work. Account for those hours in its ranking.

## One short audit, then action

Use signed-in sessions and authorised connectors first. Gather a recent complete 28-day view where available. Add the prior period when readily accessible. Useful inputs are earnings, ad delivery and page views from AdSense, search queries and coverage from Search Console, and landing-page traffic from GA4. A missing dashboard is an information gap. Continue independent work and request only the access needed for the chosen action.

Return one short ranked table with up to three recommendations. For each, record the observed problem, proposed change, traffic affected, revenue mechanism, an honest range or unknown, one-time setup, ongoing owner minutes, required approval and review date. Show the assumptions behind numerical estimates.

For an ad estimate, calculate eligible monthly views divided by 1,000, multiplied by observed incremental RPM. For bookings, use relevant visits multiplied by outbound click rate, completed-booking conversion and net commission. Keep these as sensitivity calculations until there is account data. Account for partner fees, cancellations and collection effort. Use the resulting total revenue and owner minutes together.

Prepare the code or configuration and verify the preview before the final publication or account-setting approval. Reuse the working release process. Revenue-affecting defects justify immediate diagnosis. A larger backend audit is outside this phase unless a selected action depends on it.

## Review and exit criteria

Review the shipped changes after roughly 14–28 days. Ad experiments or booking outcomes may need longer to mature. State whether traffic and completed outcomes are sufficient for a useful conclusion. A calendar date alone cannot establish an uplift.

Continue Phase 1 while a small, evidence-backed improvement fits the owner-time assumption. Move to the next phase when the selected quick fixes are operational, their revenue or lack of revenue is understood, and the remaining attractive work needs sustained traffic acquisition, content production, sales or customer handling. If traffic is insufficient, record the smallest acquisition experiment as the next-phase decision.

The later backlog contains broad social publishing, 40–60 articles, Hindi expansion, new X/Threads channels, a sales programme for directory placements and a custom automation stack. An existing asset can enter Phase 1 when it has a specific revenue case and little added work. There is no standing posting quota in Phase 1.

The recurring workflow is one brief review of earnings, relevant visits, outbound booking clicks, confirmed outcomes and owner time. Add a scheduled report only after this manual view is useful and the input access is reliable. [Scheduled tasks](https://learn.chatgpt.com/docs/automations?surface=app)

## Changes from the seed plan

Compared with the imported plan at `f68e2a5` and the engineer source at `65451b9`.

| Scale | Seed recommendation or assumption | Current treatment |
|---|---|---|
| Completed seed work | Real HTML page per place, itinerary and activity, editable content, metadata, homepage links and sitemap. | Delivered for 35 public records. These are concise launch guides. Further local detail remains editorial work. |
| Completed seed work | Remove test partners, resolve repeated strip entries and describe images. | Delivered for the partner list and attraction photos, including an admin photo-description field. Decorative background images retain empty alt text. |
| Major reprioritisation | Substantial social output alongside 40–60 pages in three months. | Concentrate first on monetising existing eligible visits and the top few commercial pages. Content volume and channel expansion enter the later backlog. |
| Major reprioritisation | Directory sales and an owner-managed enquiry flow become the main revenue opportunity after audience growth. | Compare actual return and owner hours. Start with one self-service booking route or an existing low-maintenance commercial relationship when feasible. Directory sales can win if an operator is ready and the economics work. |
| Major evidence correction | One ad slot, a much larger directory opportunity and follower targets implied likely revenue outcomes. | Use account revenue, delivery, traffic and completed bookings. The code also has a separate Ad Manager component. No stream's income potential has been established for this site. |
| Major operational addition | Optional Git-connected Cloudflare move. | Completed using Direct Upload after the Git integration failed. GitHub CI checks code, while the verified release script publishes a specific commit. Billing is handled by the owner. |
| Minor factual corrections | Fourteen attractions, SMS verification active and a new Google Business Profile as a quick win. | The public feed had 13 places. SMS is disabled. Check in-person business eligibility if a profile becomes relevant. [Google eligibility](https://support.google.com/business/answer/13763036) |
| Additional engineering | The first-visit content deadline and visited guide-link contrast were outside the seed brief. | Fixed after browser verification exposed the two issues. |
| Workflow correction | Every task was assigned Sol at Extra High based on a temporary session request. | Recommend model and effort for each task. The bounded revenue audit starts with GPT-6.2 Sol at Medium. [Model selection](https://learn.chatgpt.com/docs/model-selection) |

## Working materials

The current six-part setup and copy-paste prompt are in [working sessions](../setup/chatgpt-workflows.md). The [owner checklist](../setup/owner-inputs.md) identifies the small initial input packet and optional later channel access. [Hosting notes](git-and-hosting-plan.md) contain rollback and deployment details.
