# Current work queue

Updated 22 November 2026. This file owns live status, dependencies and owner commitments. [Start/dashboard](dir-structure.md) · [Strategy](strategy/roadmap.md) · [Next prompt](NEXT-PROMPT.md) · [Setup for review](setup/revenue-setup.md).

Statuses: **Ready** = executable; **In progress** = started; **Owner action** = needs the named owner input; **Review** = concrete prepared result; **Waiting** = external result/date; **Backlog** = not selected; **Done** = evidence recorded. Prefer the highest-return unblocked work; a blocked row does not block the whole queue.

## Ordered tasks

| ID / priority | Status and task | Next action / completion evidence | Dependency / when to revisit |
|---|---|---|---|
| T01 · 1 | **Owner action — AdSense identity.** Last confirmed Not started on 21 Nov; cousin help planned for **22 Nov**. | Owner follows [private checklist](setup/revenue-setup.md#owner-checklist); record status only, then verify account notices, ads.txt and real delivery. | Don't assume today's plan happened. Don't ask again during this preparation; revisit on owner update or the next relevant session after the planned day. |
| T02 · 2 | **Review — Regional personalised-ad setup.** Direction approved; [proposal pack](setup/revenue-setup.md#personalised-adcmp-proposal) prepared. | Inspect/save the actual supported Google draft/preview and verify the India/overseas notice, signals and mobile acceptance checks. Then review the concrete activation batch. | Browser preparation stopped before the AdSense screen; no saved CMP draft or activation claimed. Preparation can proceed while T01 waits. |
| T03 · 3 | **Review / Owner action — Viator pilot.** Direction approved; signup entry inspected. | Owner completes legal/private [onboarding](setup/revenue-setup.md#owner-checklist); obtain real generated links and pass [India-first gates](setup/revenue-setup.md#india-first-review-gates), then implement/verify the reviewed placements. | No account or paid links yet. Do not ask whether Viator is chosen again. Independent of AdSense. |
| T04 · 4 | **Waiting — Sitemap processing.** Still Couldn't fetch on 22 Nov refresh; 21 Nov Google live fetch passed. | In a later session check Success or a specific error; if persistent, investigate live fetch/hosting evidence before changes. | No owner action now. No repeated unchanged submissions or XML indexing requests. Preserve ownership file. [Evidence](reports/revenue-audit-2026-11-21.md). |
| T05 · 5 | **Waiting — Suitable guide ads.** Article loader/manual slots OFF; homepage is separate. | Review eligible content/placements and the concrete configuration, then verify real impressions/earnings after authorised activation. | T01/T02 plus rollout review. [Meaning](explanations/advertising-consent-explanation.md#what-guide-ads-remain-off-means); never pad articles or click live ads. |
| T06 · 6 | **Ready — Measurement validation.** Code shipped, fresh outcomes not checked. | Check stream/timezone, country/device mix, consented acquisition/events and internal traffic; reconcile clicks with completed outcomes, net commission/payout and effort. | Validate [audience assumptions](strategy/roadmap.md#audience-and-market); historical GA4 isn't repaired. Register dimensions only if useful. |
| T07 · 7 | **Ready — Qualified acquisition/content quality.** New-guide demand unmeasured. | Use clean available demand data. Fix Sam campfire-image/dunes-alt mismatch; check mixed/weak listings and local facts before commercial featuring. | Re-rank by expected return. No quotas, unapproved live-record changes or operator outreach. |
| T08 · 8 | **Backlog — Useful review/automation.** Revenue uplift not established. | Review mature outcomes; automate repeated link checks/reporting/reconciliation when useful. | No schedule without a scheduling request. Dates/counts are not hard stop rules. |

## Approval ledger

| Date | Owner decision | Meaning / boundary |
|---|---|---|
| 21 Nov | Publish tested site changes and set up Search Console | Completed: site PRs 6/7 and property verification/submission; evidence in WORKLOG/report. Reuse this result rather than ask to repeat setup. |
| 22 Nov | “Go ahead with Viator and personalised ads … Prepare the setup for review” | Chosen directions and preparation authorised. Does not mean signup terms were accepted, private fields were furnished, a Google message was published or guide ads were enabled. |
| 22 Nov | India-first audience direction | Audience direction accepted; the assumption and validation limits are maintained in [strategy](strategy/roadmap.md#audience-and-market). |
| 22 Nov | Reorganise docs and add a universal documentation rule | Current business documentation cleanup and local Codex global guidance authorised. Other existing project repositories are not being rewritten in this task. |

## Recently completed

| Result | Evidence |
|---|---|
| Shared-record cleanup and entry/naming reassessment | Five top-level records, human continuation path including NEXT-PROMPT, redundant HANDOFF removed and links updated; [22 Nov trail](WORKLOG.md). Revenue task priorities and approvals unchanged. |
| 35 crawlable guides, deployed site and automatic checked releases | WORKLOG milestone trail; technical commands in site README. |
| Four commercial-guide improvements and analytics fixes | Site PR 6, main `2939ebb`; production checks passed. |
| Search Console ownership and sitemap submission | Site PR 7, main `c427046`; verification/live-fetch evidence in the audit. Processing remains T04. |
| Owner explanations and initial queue | Business `f03fe41`; explanations remain conceptual references, not live status stores. |

When a task completes, move its evidence to WORKLOG and shorten/remove its active row. Re-rank remaining work. Keep the directory dashboard as a brief linked snapshot rather than copying this table there.
