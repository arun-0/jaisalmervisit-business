# Jaisalmer Visit — start here

Updated 22 November 2026. [Jaisalmer Visit](https://jaisalmervisit.com/) is a mobile-first travel guide and local-provider directory. Our goal is additional **net revenue**, useful travel information and reasonable owner effort. The commercial approach is to repair ad delivery, pilot disclosed booking referrals, then improve acquisition and conversion using evidence. [India-first audience assumption and strategy](strategy/roadmap.md#audience-and-market).

## Read these top-level files

The human reading path is **this page → TODO → NEXT-PROMPT**: understand the project, see current actions, then see how to continue with AI. Completing the owner steps in TODO also moves the project forward. If you only want a status check, the first two suffice. For reasons behind a decision, open the relevant WORKLOG entry. Assistants additionally load AGENTS and relevant history before work.

| File | Its distinct question / purpose |
|---|---|
| **[dir-structure.md](dir-structure.md)** | What is this project, where is everything, and where are we now? Human start page and bottom dashboard. |
| **[TODO.md](TODO.md)** | What should happen next, who owns it, what is blocked or approved, and when may we ask again? Sole current queue. |
| **[WORKLOG.md](WORKLOG.md)** | What changed or was decided, why, how was it verified, and what does it mean? Dated trail; read relevant entries. |
| **[AGENTS.md](AGENTS.md)** | How must assistants work, respect approvals and maintain these records? Rules, not a project-status summary. |
| **[NEXT-PROMPT.md](NEXT-PROMPT.md)** | How do we resume in the right app/project/model, with what exact prompt and stopping point? Reusable six-part setup. |

These five files live directly in the **business repository root**, `C:\dev\ai\ghanu-jaisalmer-visit\business`. Each owns one job and links to detail; “independent” does not mean copying all project facts into each file. `README.md` is the conventional discovery pointer and `CLAUDE.md` imports the shared assistant rules. They add no separate state or mandatory reading. There is no separate handoff file: these five records provide the handoff.

## Where the project lives

Parent workspace: `C:\dev\ai\ghanu-jaisalmer-visit`. It contains two separate private Git repositories, not one combined repository:

| Checkout | Role / repository |
|---|---|
| `business\` | Shared purpose, plans, approvals and owner/assistant records. [jaisalmervisit-business](https://github.com/arun-0/jaisalmervisit-business). |
| `site\` | Website source, editable guides, generated HTML, checks and releases. [jaisalmervisit-site](https://github.com/arun-0/jaisalmervisit-site). Its [README](../site/README.md) owns technical operation; its AGENTS adds site-specific rules. |

The homepage supplies maps, itineraries, audio, Tourist Mode and provider enquiries. Separate static guides supply ordinary place/activity/itinerary URLs. Cloudflare serves the frontend; Firebase supplies backend services. [Hosting/recovery reference](strategy/hosting-operations.md).

## Detail map

| Business folder | What belongs here / useful entry |
|---|---|
| `strategy/` | Commercial direction in [roadmap.md](strategy/roadmap.md); operating/recovery facts in [hosting-operations.md](strategy/hosting-operations.md). |
| `setup/` | Execution detail: [revenue setup/owner checklist](setup/revenue-setup.md), [access/privacy reference](setup/owner-inputs.md), [using another assistant](setup/assistant-portability.md). |
| `explanations/` | Concepts and trade-offs: [affiliates](explanations/affiliate-pilot-explanation.md), [ads and consent](explanations/advertising-consent-explanation.md). |
| `reports/` | Dated observations, not live status: [21 November revenue audit](reports/revenue-audit-2026-11-21.md). |
| `content/` | [Editorial/implementation brief](content/engineer-brief.md); editable public guide content is in `site/content/`. |
| `social/` | [Acquisition approach/profile drafts](social/social-media-plan.md) and [unscheduled draft bank](social/draft-bank.md). No publishing approval implied. |

Original seeds/private transcripts remain local under the parent workspace's `seed-resource/`; they are not active instructions or shared records. Keep private/raw exports ignored. Current facts belong in their designated home above; this page carries only a linked snapshot.

## Very short journey

| Milestone | What it means / detail |
|---|---|
| 20 Nov: shared two-repository handoff | Collaboration moved into shared files. [Trail](WORKLOG.md). |
| 21 Nov: 35 guides and checked automatic releases | Crawlable content and repeatable publication exist. [Technical README](../site/README.md). |
| 21 Nov: commercial-guide/analytics fixes and account audit | Published improvements; small observed audience and monetisation gaps identified. [Audit](reports/revenue-audit-2026-11-21.md). |
| 21 Nov: Search Console verified; sitemap submitted | Ownership is complete; submission does not establish processing or indexing. [T04](TODO.md). |
| 22 Nov: Viator/personalised-ad direction; records clarified | Setup prepared for review; private onboarding and concrete activation remain separate. [Trail](WORKLOG.md) and [review pack](setup/revenue-setup.md). |

## Owner dashboard

Snapshot: 22 November 2026. **[TODO.md](TODO.md) is authoritative** if this summary and live status differ.

| View | Concise result / next step |
|---|---|
| Done | Guides and analytics fixes published; Search Console verified/submitted; documentation cleaned and setup pack prepared. [Evidence/trail](WORKLOG.md). |
| You next | T09: choose the GitHub access route. T01: reconcile the cousin’s prior-verification confirmation with the live AdSense hold. T03: Viator terms/signup/private profile. T02: review the concrete ad batch when ready. [Exact owner checklist](setup/revenue-setup.md#owner-checklist). |
| Independent AI work | T02: actual regional-consent draft/preview and notice preparation. T06–T07: measurement and targeted content checks. Affiliate preparation can proceed while onboarding waits. [Priority/dependencies](TODO.md). |
| Blocked / waiting | T04 sitemap processing unresolved. T05 article/“guide” ads OFF pending account, consent, content and rollout review. No paid affiliate links or saved consent draft yet. [Current queue](TODO.md). |
| Next prompt | [NEXT-PROMPT.md](NEXT-PROMPT.md). Respect recorded owner dates/conditions and existing approvals; a passed date is not proof of completion. |
