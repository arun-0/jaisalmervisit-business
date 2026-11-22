# Project trail — what changed and what it means

Newest first. Live statuses, owner commitments, approvals and follow-up dates belong in [TODO.md](TODO.md); this file records significant events and their meaning. [Project dashboard](dir-structure.md) · [Dated account evidence](reports/revenue-audit-2026-11-21.md).

## 22 November 2026 — Public repositories, owner-only main and cousin invitations

**Decision / change:** Owner explicitly authorised making both repositories public to enable main restrictions without a paid upgrade. Applied public visibility, then active exact-main creation/update/deletion rules with only the explicit `arun-0` user able to bypass. Only after read-back verification, sent write invitations to `jaisalmer-visit` for both repositories. Invitations were pending at verification; no effective collaborator write access is claimed yet.

**Verification:** Before publication, reviewed tracked/historical file names and ran Gitleaks 8.30.1 on reachable local Git history (`--all`): business had zero findings; site's three findings were reviewed as Firebase browser configuration, a cache label and public audio download links, not administrator/deployment credentials. Private raw files/seeds/transcripts were not tracked. This is a scoped review, not a guarantee against every possible exposure. GitHub API read-back confirmed public visibility, active rulesets business `27849265` / site `27849267`, all three effective rules and a sole named-user owner bypass; invitations reported write and current public-only permission read. No billing, ownership, DNS, live Firebase or ad changes were made.

**Release/follow-through:** Business `c4c0037` pushed through the intended named-owner bypass. Site [PR 9](https://github.com/arun-0/jaisalmervisit-site/pull/9) corrected one README visibility reference; checks passed. Ordinary merge was blocked by the new policy, then authenticated `arun-0` merged with the explicit owner bypass, main `5b9180b`. [Run 45048170727](https://github.com/arun-0/jaisalmervisit-site/actions/runs/45048170727) passed checks, automatic deployment and published-release verification; public application assets match the previous release. After the owner reported missing invitations, API recheck confirmed both targeted `jaisalmer-visit`, write permission, not expired, created 22 Nov at 17:11 UTC. Shared their exact GitHub-provided acceptance links without cancelling or duplicating invitations. Final effective permissions: jaisalmervisit-business: read, pending=True; jaisalmervisit-site: read, pending=True. Current acceptance state belongs in T09/completed queue.

**Meaning:** Anyone can read/clone repository contents and history. Cousin can contribute topic branches once invitations are accepted; only the owner can update/merge main. The earlier plan-capability blocker is resolved. T09 now tracks acceptance only. [Operating configuration](strategy/hosting-operations.md#collaboration-and-main-branch-control). Updated current visibility/instruction text; earlier dated private-repository observations remain historical.

## 22 November 2026 — Write access approved with owner-controlled main

**Decision:** Owner approved cousin `jaisalmer-visit` receiving read/write access to both repositories, with only owner `arun-0` updating main directly and other contributors using pull requests. This supersedes the earlier read-only request.

**Evidence / blocker:** Authenticated as `arun-0`, confirmed administrator capability, private repositories and default main branches. Both repositories returned HTTP 403 for both ruleset and classic branch-protection endpoints, explicitly requiring GitHub Pro or public visibility. Pending invitation lists were empty. Account-plan metadata was unavailable through the current token, so no particular billing plan is claimed beyond the feature rejection. GitHub's documented private-repository plan limitation corroborates the error.

**Changed / meaning:** Recorded the owner-only main policy in shared rules and prepared the exact restrict-updates/admin-owner bypass sequence in [hosting operations](strategy/hosting-operations.md#collaboration-and-main-branch-control). No invitations were sent because granting write before enforcing the attached main restriction would violate the requested outcome. No billing, visibility, ownership or protection setting changed. T09 waits for plan capability, not another write-access approval; normal owner-authenticated record commits remain authorised. Local link/anchor and diff checks passed before push.

## 22 November 2026 — Cousin repository access checked

**Request / evidence:** Owner requested read access for cousin's GitHub account `jaisalmer-visit` to both private repositories. Authenticated GitHub API confirmed the account, both repositories owned by personal user `arun-0`, administrator capability for the current operator and no existing collaborator permission for the cousin. [GitHub's documented personal-repository roles](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/permission-levels-for-a-personal-account-repository) only allow collaborator read/write, not read-only.

**Meaning / next condition:** No invitation, access expansion, ownership transfer or deployment change was made. T09 records the owner choice between explicitly authorising read/write invitations and reviewing an organisation route for true read-only access. The request for read access is not permission to broaden it to write.

## 22 November 2026 — Identity verification claim cross-checked

**Changed / why:** Owner reported the cousin/site owner completed verification before this project. Rechecked the existing signed-in AdSense publisher against the website seller line, Home, Verification check and the linked India payments account. Live UI still reports identity Needs attention, a payments hold and a 21 December serving deadline. [Dated observations and limits](reports/adsense-identity-check-2026-11-22.md).

**Meaning / correction:** The earlier Not started wording was directly present in AdSense; it does not prove no previous verification happened. The current notice and owner's report conflict. T01 now asks to reconcile service/account/prior success, superseding the old planned cousin-help step, rather than request duplicate documents. Detailed payment/serving status is more precise than treating identity as the established sole reason for zero delivery. Updated the owner checklist/dashboard; no private submission, account change or ad activation occurred. Local document/anchor and whitespace checks passed before commit/push.

## 22 November 2026 — Human continuation path and redundant handoff removed

**Changed / why:** Corrected the earlier wording: the human continuation path includes dir-structure, TODO and NEXT-PROMPT. The first two answer a status-only check; NEXT-PROMPT supplies the exact setup for advancing with AI. Owner actions in TODO also advance the project independently. Removed business/HANDOFF.md because it only repeated entry links and had no unique content or current inbound document links. README remains the conventional repository discovery pointer; the five primary records collectively provide handoff.

**Verification / meaning:** Reviewed current business references and companion site entry references; checked all 18 remaining business documents and local links/anchors plus whitespace/diff checks before push. Historical trail references describe the earlier file accurately and remain unchanged; its content is recoverable from Git. Revenue tasks, approvals and website behaviour are unchanged.

## 22 November 2026 — Start-page reassessment and useful naming

**Assessment / why:** The prior start page covered purpose, journey and dashboard, but left the reading order implicit and buried the continuation prompt. Some legacy filenames described an old calendar/tutorial/plan rather than their current content. Cosmetic hyphen-to-underscore renaming would add churn without improving meaning.

**Changed:** Added a five-file reading guide and explicit business-root versus parent-workspace distinction. Kept `dir-structure.md`, AGENTS, TODO and WORKLOG; promoted the session setup to top-level `NEXT-PROMPT.md`. Renamed README.txt → README.md for conventional repository discovery, setup/claude-account-setup.md → setup/assistant-portability.md, social/calendar-2026-11-week1-2.md → social/draft-bank.md, and strategy/git-and-hosting-plan.md → strategy/hosting-operations.md. Updated current links and naming rules; historical source URLs still point to the original names at their original commit. HANDOFF and CLAUDE remain compatibility pointers, not additional state stores.

**Verification:** Reviewed the start page against the owner's [2][a]–[e] requirements: durable rule/trail, concise purpose/journey/next prompt, bottom owner dashboard, distinct authoritative homes and reduced duplication. All 19 business documents and their local links/anchors passed validation; `git diff --check` passed. No current local links retain the old paths; historical source URLs intentionally do. No website or monetisation settings change in this unit.

**Meaning:** A human can catch up from the start page and TODO; an assistant also loads rules, relevant history and the exact next prompt. All five primary records are top-level in the shared business repository, with detail linked below. Older filename links outside the repository may need the new names; the Git history is retained.

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

**Evidence:** Source import `65451b9`, business seed `f68e2a5`; guide release `3fd8ad8` with verified deployment `d763e7bf`. Automatic checked main deployment followed in PR 5/main `b64961b`, run `44943644703`, deployment `4aab1457`. Domain/rollback details are in [hosting notes](strategy/hosting-operations.md).

**Meaning:** Main pushes deploy after checks, so site publication needs the applicable concrete authorisation. Firebase billing was confirmed handled. Direct Upload/CI was chosen after Cloudflare Git integration failed, not because the backend moved.

## 20 November 2026 — Shared business handoff established

**Changed:** Owner and Claude assembled business/social/technical drafts, handoff, two-repository plan and shared instructions for the brother.

**Meaning:** These were proposals and initial assumptions, not evidence of posts, earnings, paid partners or account activation. Current strategy and TODO supersede old quotas, dates, unsupported platform claims and setup assumptions.

## Maintaining this trail

For each significant unit, record **date → what/decision → why/evidence → meaning**, with links and commit/run references where useful. Put current next actions only in TODO. Keep routine repeated checks concise. Original pre-cleanup documents and the longer session-style worklog remain in [Git history at f03fe41](https://github.com/arun-0/jaisalmervisit-business/tree/f03fe41); private transcripts remain outside Git.

WhatsApp handover: “Start at dir-structure.md; TODO owns current work, WORKLOG explains the journey. Viator/personalised-ad preparation is approved; owner private signup/identity and concrete activation review remain.”
