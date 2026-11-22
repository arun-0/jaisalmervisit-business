# Project trail — what changed and what it means

Newest first. Live statuses, owner commitments, approvals and follow-up dates belong in [TODO.md](TODO.md); this file records significant events and their meaning. [Project dashboard](dir-structure.md) · [Dated account evidence](reports/revenue-audit-2026-11-21.md).

## 22 November 2026 — Review preparation and documentation organisation

**Decision:** Owner chose Viator and personalised ads with consent, asking for setup preparation and review rather than claiming activation. Owner also authorised a universal documentation rule and cleanup of the project records, and clarified India-first visitor optimisation (roughly 95% as an assumption to validate, regardless of the owner’s UK location).

**Changed:** Established the directory reference as the human entry/dashboard, TODO as the sole live queue, this trail for decisions/results/meaning, and the roadmap for strategy. Reviewed all tracked business records, including historical social/setup drafts, and the relevant site instructions/README/privacy/analytics/build material. Kept generated HTML/assets, source originals and private seed archives in their technical/reference roles rather than rewriting them as documentation. Consolidated duplicated setup/status into those homes and prepared `setup/revenue-setup.md`. Kept explanations conceptual, reports factual, and social material explicitly unscheduled. Updated global local-Codex guidance while preserving existing personal preferences.

**Evidence / limit:** Viator's signup screen showed Email → Create account, with acceptance of terms by proceeding. No private details or signup submitted. Browser control stopped before AdSense preparation could continue because it could not reliably establish the current URL. The CMP package is therefore a specified proposal, not a saved account draft or live setting. Sitemap refresh still showed Couldn't fetch. Review added India-specific INR/payment/pickup/cancellation gates; UPI and domestic checkout are unverified. Code review found existing analytics/privacy copy assumes non-personalised ads; T02 includes correcting that before activation.

**Verification:** Checked all 19 project documents and 96 local links/anchors, preserved the prior global preferences, and passed whitespace/diff checks. Business cleanup was pushed as `d868468`. Companion [site PR 8](https://github.com/arun-0/jaisalmervisit-site/pull/8), main `bcd1255`, only links its technical records to the shared entry/queue. Both PR checks passed; [main run 45041038989](https://github.com/arun-0/jaisalmervisit-site/actions/runs/45041038989) passed checks, automatic deployment and published-release verification. Public assets, content and monetisation configuration match the prior published source.

**Meaning:** Future assistants can recover purpose, state, approvals and the next unblocked action from files without a transcript. The owner still completes private/legal account actions and reviews the concrete ad rollout. T01–T08 own the follow-up; the documentation-only main merge republished the same public source; it made no new ad-account, affiliate, access or scheduled change.

## 21 November 2026 — Commercial guides and Search Console published

**Changed:** With explicit owner approval, site PR 6/main `2939ebb` published Sam, Khuri, camel/jeep-safari improvements, guide-click events and analytics consent/source fixes. PR 7/main `c427046` added Google's retained HTML ownership file. Search Console URL-prefix ownership was verified and the 37-URL sitemap submitted.

**Evidence:** Actions `44947673883` and `44947905108` passed check/deploy; production checks covered 35 guides, 37 sitemap URLs and 14 assets. Google's 20:48 GMT live test found the sitemap available, while its separate processing report showed Couldn't fetch. [Audit](reports/revenue-audit-2026-11-21.md).

**Meaning:** The release and ownership setup are completed; don't repeat their approval requests. Live fetch is different from processing/indexing. Guide Auto ads remained OFF, with a tested independent control ready for later review. No affiliate or ad-account activation occurred.

## 21 November 2026 — Revenue evidence and initial opportunity selection

**Changed:** Inspected signed-in AdSense/GA4, search access and public delivery. Added conceptual owner explanations and an ordered opportunity queue (business `f03fe41`).

**Evidence:** AdSense Ready/Auto ads ON but zero delivery in Last 30 days; identity Not started, ads.txt warning despite correct responses, no published Google European message, one unfilled live slot. GA4 24 Oct–20 Nov: 176 sessions, 403 views, 43 active users, internal UI names appearing in source/medium. [Full evidence and limits](reports/revenue-audit-2026-11-21.md).

**Meaning:** Fix account/consent and establish a paid booking route, but don't forecast substantial passive income from the small observed audience. Clean future measurements rather than pretend historical attribution is repaired. Owner planned cousin help for identity on 22 Nov; current status is T01, not an assumed completed action.

## 21 November 2026 — Website foundation and repeatable releases

**Changed:** Imported separate private business/site repositories, shipped 35 editable static guides and the 37-URL sitemap, removed repeated/demo partner output and added image descriptions. Improved delayed/offline/stalled public-data loading and guide-link contrast. Moved the static frontend to Cloudflare Pages while retaining Firebase services/fallback.

**Evidence:** Source import `65451b9`, business seed `f68e2a5`; guide release `3fd8ad8` with verified deployment `d763e7bf`. Automatic checked main deployment followed in PR 5/main `b64961b`, run `44943644703`, deployment `4aab1457`. Domain/rollback details are in [hosting notes](strategy/git-and-hosting-plan.md).

**Meaning:** Main pushes deploy after checks, so site publication needs the applicable concrete authorisation. Firebase billing was confirmed handled. Direct Upload/CI was chosen after Cloudflare Git integration failed, not because the backend moved.

## 20 November 2026 — Shared business handoff established

**Changed:** Owner and Claude assembled business/social/technical drafts, handoff, two-repository plan and shared instructions for the brother.

**Meaning:** These were proposals and initial assumptions, not evidence of posts, earnings, paid partners or account activation. Current strategy and TODO supersede old quotas, dates, unsupported platform claims and setup assumptions.

## Maintaining this trail

For each significant unit, record **date → what/decision → why/evidence → meaning**, with links and commit/run references where useful. Put current next actions only in TODO. Keep routine repeated checks concise. Original pre-cleanup documents and the longer session-style worklog remain in [Git history at f03fe41](https://github.com/arun-0/jaisalmervisit-business/tree/f03fe41); private transcripts remain outside Git.

WhatsApp handover: “Start at dir-structure.md; TODO owns current work, WORKLOG explains the journey. Viator/personalised-ad preparation is approved; owner private signup/identity and concrete activation review remain.”
