# Jaisalmer Visit working rules

Read [dir-structure.md](dir-structure.md), [TODO.md](TODO.md) and the newest [WORKLOG.md](WORKLOG.md) entry before substantive work. These records must let the owner, brother or another assistant resume without the chat transcript.

## Documentation contract

- `dir-structure.md`: the human entry point, file map, concise journey and bottom owner dashboard. Link to detail; do not turn it into another worklog or task list.
- `TODO.md`: the only current task/status, dependency, owner-action, approval and deferred-follow-up queue. Work the highest-value unblocked item. Respect its check-after dates and conditions; do not repeat a question before it becomes actionable. Passing a date does not mean the owner completed an action.
- `NEXT-PROMPT.md`: top-level reusable six-part continuation setup; keep current task status in TODO, not in the prompt.
- `WORKLOG.md`: the dated trail of what changed, why, evidence and practical meaning. Add an entry for a meaningful decision, implementation, verification, release or handoff; use task IDs instead of copying current task tables.
- `strategy/roadmap.md`: objective, prioritisation and commercial strategy. `setup/`: execution and private owner-input instructions. `explanations/`: owner-facing meanings and trade-offs. `reports/`: dated evidence. Each fact belongs in its appropriate home; summaries link there.
- Keep the five primary entry records directly in this repository root with distinct purposes. Use established uppercase control filenames; use lowercase kebab-case for descriptive documents and ISO dates for dated evidence. Keep the established `dir-structure.md` name; do not create a competing underscore or START-HERE copy. README is a discovery pointer only; the five primary records provide handoff without a separate HANDOFF.md. Human continuation guidance must include NEXT-PROMPT alongside the start page and TODO.
- Reconcile these records after meaningful work. Mark recommendations, owner decisions, prepared drafts and published results distinctly. Remove stale duplicated status; preserve significant history in the worklog/Git. Update the directory map after file-role changes.
- Give a concise six-part setup when recommending a new/resumed/handoff workflow: chat, app, full project path, available model/effort, exact prompt, follow-up/stop point. The reusable setup is [here](NEXT-PROMPT.md). Use chat questions here; popup questions have disappeared before the owner could answer.

## Work and verification

Prioritise expected net revenue, traveller usefulness, effort and recurring owner work. Let evidence and owner feedback change the order. Manual pilots and progressive automation are both useful; page counts, review minutes and perfect measurement are not gates.

Use existing authorised sessions/tools first. Pull before edits, verify proportionately, commit and push relevant work with the configured human identity and no AI attribution. On Windows use Git Bash, uv for Python and fnm for Node; on another OS use its authorised equivalent and establish actual paths. Site code/instructions are in the sibling `site` checkout; use its topic-branch and release process.

## Taking turns across two repositories

“Pull latest and do next” invokes this contract for both owner and contributor; identify the active GitHub role rather than infer it from a browser login or Git author. Use `arun-0` for owner operations and `jaisalmer-visit` for cousin contributor operations. Keep the configured human commit identity and never add AI co-author/attribution trailers.

1. Inspect both working trees and branches; fetch both repositories. Preserve local changes/unfinished branches. Fast-forward clean main checkouts only; never reset or overwrite work just to pull. Inspect open PRs in **both** repositories before choosing a task: main alone does not contain unmerged work.
2. Read the entry, TODO, newest relevant trail and any open-PR handover. Highest-value unblocked work comes next, but do not duplicate a task already underway/under review. Work sequentially by default. If both people intentionally overlap, agree distinct task IDs/files first; an unmerged branch is not a global task lock.
3. Use a topic branch per coherent turn/task in each changed repository, e.g. `cousin/T07-sam-image` or `owner/T06-measurement`. Task ownership, In progress/Review status and branch/PR links belong in TODO; update WORKLOG with decisions, evidence and meaning. A queue change still in a PR is proposed until merged. Do not invent permanent extra handoff files.
4. Contributor: verify, commit and push **every changed repository**, then open PRs to main; cross-link the source and business-record PRs when paired. Put task ID, what/why, checks, approvals/dependencies and exact next action in each PR description. Mark work Review/prepared, not merged/published. Leave both working trees clean or explicitly explain any preserved unfinished changes. Stop at the review-ready handover; never merge/push main or deploy independently.
5. Owner: inspect and review the incoming PRs before starting more work. Run appropriate checks and resolve conflicts without discarding either person's work. Merge only within existing authorisation; hold consequential unapproved changes for a concrete decision. Source first where business completion depends on a site release; verify the authorised deployment, then reconcile/merge the corresponding record changes. Owner credentials and configured bypass are required for main updates; check success instead of assuming PR merge means deployment passed.
6. Finish with pushed branch/PR or merged commit references, checks, remaining owner/private steps and the exact next action. Current state stays in TODO, decisions/results in WORKLOG, prompts in NEXT-PROMPT. Next person fetches both repositories and checks PRs again; neither chat transcript nor local memory is the shared state.

## Authority and private material

Only repository owner `arun-0` may directly update or merge into `main` in either repository. Other collaborators work on topic branches and open pull requests for the owner to review/merge. An assistant using another collaborator’s credentials must not bypass this policy. Current GitHub enforcement/access status is in T09; a written rule does not prove server-side protection.

Reuse explicit approvals recorded in TODO/worklog; do not ask again merely because a task resumes. Prepare a concrete reviewable result before a necessary final approval. Apply higher-priority action-time rules when relevant. A request to prepare a setup is not a claim that an account, contract, ad setting or public release has been activated.

Outbound posts/messages/operator contact, payments, new account/ad settings and named-domain production/DNS releases need the applicable explicit authorisation. Keep passwords, OTPs, tokens, IDs, banking details, private visitor data and transcripts out of Git/chat. The actual owner/payee handles private/legal submissions; family assistance is not a change of account identity. Do not invent invitations or schedules.

Use the [site README](../site/README.md) for runtime/build behaviour and [hosting notes](strategy/hosting-operations.md) for recovery. Use dated/local sources for travel facts, inventory and prices. Never equate an enquiry with a booking, a loaded ad script with revenue, or sitemap submission with indexing.
