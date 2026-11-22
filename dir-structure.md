# Jaisalmer Visit — start here

Updated 22 November 2026. A mobile-first Jaisalmer guide and local-provider directory at [jaisalmervisit.com](https://jaisalmervisit.com/). The business goal is additional net revenue with useful travel information and reasonable owner effort. **Audience: India-first.** The owner’s planning assumption and validation limits live in [the strategy](strategy/roadmap.md#audience-and-market).

Project: `C:\dev\ai\ghanu-jaisalmer-visit`. Two sibling private repositories:

| Checkout | Purpose | Repository |
|---|---|---|
| `business\` | Instructions, live todo, decision trail, setup, explanations and evidence | [jaisalmervisit-business](https://github.com/arun-0/jaisalmervisit-business) |
| `site\` | Public website source, guide Markdown, generated HTML, checks and deployment | [jaisalmervisit-site](https://github.com/arun-0/jaisalmervisit-site) |

## Directory map

```text
business/
├── AGENTS.md                 # how assistants work and maintain records
├── CLAUDE.md                 # imports AGENTS.md
├── dir-structure.md          # this owner/AI entry point
├── TODO.md                   # sole live task/status/owner/dependency queue
├── WORKLOG.md                # dated changes, decisions, evidence and meaning
├── HANDOFF.md / README.txt   # short entry pointers
├── strategy/
│   ├── roadmap.md            # revenue strategy and prioritisation
│   └── git-and-hosting-plan.md # operating/recovery reference
├── setup/
│   ├── revenue-setup.md      # exact Viator/CMP review pack and owner steps
│   ├── chatgpt-workflows.md  # six-part session setup and exact next prompt
│   ├── owner-inputs.md       # evidence/privacy/access reference
│   └── claude-account-setup.md # portable assistant entry guidance
├── explanations/
│   ├── affiliate-pilot-explanation.md
│   └── advertising-consent-explanation.md
├── reports/
│   └── revenue-audit-2026-11-21.md # dated account/release evidence
├── content/
│   └── engineer-brief.md     # delivered foundation and remaining editorial brief
└── social/
    ├── social-media-plan.md  # optional acquisition approach and profile drafts
    └── calendar-2026-11-week1-2.md # unscheduled idea/draft bank
```

This is the canonical directory reference; retain the established hyphenated filename rather than create a duplicate `dir_structure.md`. Site file/build/runtime details belong in [site/README.md](../site/README.md). Original seeds/private transcripts remain local under `seed-resource/`; they are not active project instructions or shared records. Raw exports belong only in ignored private/raw folders when needed.

## What the project does and how it reached here

The interactive homepage supplies maps, itineraries, audio, Tourist Mode and local-provider enquiries. Separate static guides make content reachable at ordinary place/activity/itinerary URLs. Cloudflare serves the website; Firebase still supplies the backend. [Technical operating reference](strategy/git-and-hosting-plan.md).

| Milestone | Practical meaning / detail |
|---|---|
| 20 Nov: shared plans and repository handoff | Owner/brother can collaborate from files. [Trail](WORKLOG.md). |
| 21 Nov: 35 guides, sitemap, partner cleanup and checked automatic deployment | Crawlable content and repeatable releases exist; this does not prove indexing or income. [Site README](../site/README.md). |
| 21 Nov: account audit, commercial-guide and analytics fixes | Small measured baseline; monetisation and clean future measurement need follow-through. [Audit](reports/revenue-audit-2026-11-21.md). |
| 21 Nov: Search Console ownership and submission | Ownership is verified; sitemap processing is still a separate pending result. [T04](TODO.md). |
| 22 Nov: Viator/personalised-ad direction and clearer records | Prepare setup for review, with private/legal owner actions separated from implementation. [Review pack](setup/revenue-setup.md). |

## Where facts belong

[TODO](TODO.md) owns current status/commitments/approval conditions; [WORKLOG](WORKLOG.md) explains changes and why; [roadmap](strategy/roadmap.md) explains commercial direction; [setup](setup/revenue-setup.md) gives execution detail; [explanations](explanations/affiliate-pilot-explanation.md) explain concepts; [audit](reports/revenue-audit-2026-11-21.md) supplies dated evidence. This page is a concise derived dashboard, not a second detailed status store.

## Owner dashboard

| View | Concise status / link |
|---|---|
| Done | Site foundation and guide/analytics changes published; Search Console verified/submitted; records cleaned and setup review pack prepared. [Trail](WORKLOG.md). |
| Your next actions | Complete AdSense identity with the correct payee; review Viator terms/signup/private profile; review the concrete ad setup when ready. [Exact owner checklist](setup/revenue-setup.md#owner-checklist). |
| AI can move now | Prepare India-first affiliate placements and regional consent/notice changes; validate measurement and targeted content. [Ordered queue](TODO.md). |
| Waiting / deliberately off | Sitemap processing unresolved; guide ads OFF pending the reviewed account/content/consent rollout; no affiliate account/paid links or saved CMP draft claimed. [T02–T05](TODO.md). |
| Resume | Read this page → TODO → newest WORKLOG entry, then the linked setup. [Exact six-part setup and prompt](setup/chatgpt-workflows.md). Respect deferred dates/conditions; don't ask completed approvals again. |
