# Continue the revenue work

Current work and approvals live in [TODO](TODO.md); working rules and the turn-taking contract live in [AGENTS](AGENTS.md#taking-turns-across-two-repositories). Read [the project entry](dir-structure.md) and relevant [trail](WORKLOG.md) first. Both people use the same Git records; chats and local browser logins are not shared memory.

## Owner — Codex

| Setup item | Use |
|---|---|
| Chat | Same chat for one turn and its review. Start fresh when unrelated history becomes costly; use the saved records. |
| App | Local Codex desktop. |
| Project / full path | `ghanu-jaisalmer-visit` — `C:\dev\ai\ghanu-jaisalmer-visit`; business and site are sibling repositories. |
| Model / effort | GPT-6.2 Sol · Medium for routine work; practical recommendation, not a proven cost optimum. |
| Exact prompt | Owner prompt below. Later shorthand: **Pull latest and do next.** |
| Follow-up / stop | Keep review/fixes in this chat. Merge only work within recorded authorisation after review/checks; stop for a missing consequential approval or private/legal owner step, while continuing independent work. |

```text
Pull latest and do next on Jaisalmer Visit as owner arun-0.
Read business/AGENTS.md, business/dir-structure.md, business/TODO.md,
the newest WORKLOG entry and relevant setup; read site/AGENTS.md
and site/README.md before site work.

Check local changes and GitHub identity first. Fetch both repos and
inspect open PRs and their handovers before choosing a task. Review
the cousin's work, run the relevant checks, and merge only within
existing approvals using owner credentials. Resolve records and
verify any authorised deployment before calling it published.
If review needs a decision, explain the concrete issue and continue
independent work. Do not blindly merge or discard local changes.

Then take the highest-value unblocked TODO, preserving the India-first
strategy, approvals and owner check-after conditions. Verify, commit,
push and leave a clear handover in the shared records and PRs.
Do not request private documents or accept legal terms for anyone.
```

## Cousin — Claude Code

| Setup item | Use |
|---|---|
| Chat | Fresh local Claude Code session in an empty/existing parent folder for the bootstrap; keep setup follow-ups together. After readiness is verified, continue the contributor turn in the same session or reopen business with site allowed. Later turns can use a fresh session reading the same records. |
| App | **Local Claude Code**, signed in with the cousin's Claude Pro subscription; not an ordinary browser chat without repository write tools. |
| Project / full path | Bootstrap folder: `C:\dev\ai\ghanu-jaisalmer-visit` (create/select it first). Resulting working checkout: `C:\dev\ai\ghanu-jaisalmer-visit\business`, with sibling `site` allowed. This is a proposed path on his machine, not a claim it exists. If his OS/path differs, establish the actual absolute path before work. [First-time setup](setup/assistant-portability.md). |
| Model / effort | Recommend **Sonnet 5.5 (`claude-sonnet-5-5`) · Medium**: select through `/model`, then `/effort medium`. Verify his offered models; do not assume account availability. If absent, report the menu and choose a supported Sonnet/Medium option. Ordinary work does not call for maximum effort. |
| Exact prompt | **First-time bootstrap prompt below needs no clone.** After readiness, use the contributor prompt; later **Pull latest and do next as contributor jaisalmer-visit** invokes the same contract. |
| Follow-up / stop | Bootstrap stops at verified setup, before project edits/pushes. Say **Setup verified; start my contributor turn using NEXT-PROMPT.md** to proceed. Contributor turns complete a useful coherent task and its checks, commit/push branches and open linked PRs. Stop that turn at review-ready PR handover; use **Address the review comments on these PRs** for fixes. Do not merge/push main or deploy independently. No arbitrary page/time cap. |

### First session — bootstrap

```text
Set up Jaisalmer Visit on this computer from scratch. Do not assume
GitHub CLI is installed or either repository is already cloned.
I use Claude Pro and GitHub account jaisalmer-visit; arun-0 owns main.

First identify the OS, current folder and existing git/gh tools.
On Windows use Git Bash. Use C:\dev\ai\ghanu-jaisalmer-visit as
the proposed parent; if this machine uses another OS/path, establish
the actual absolute path. Inspect/reuse existing checkouts safely.
Install only missing tools from official sources. If a PATH refresh
or human installation step is needed, give the exact step and resume.

Authenticate GitHub CLI using:
gh auth login --hostname github.com --git-protocol https --web
Let me complete browser/device authentication privately as
jaisalmer-visit. Never request or print passwords, tokens or OTPs.
Check gh api user --jq .login before writes; don't reuse arun-0's
credentials. Configure Git's GitHub credential helper with
gh auth setup-git. Preserve my human Git author identity; if absent,
ask for my preferred name/email and configure it only in these repos.

Clone only missing repositories into sibling directories:
https://github.com/arun-0/jaisalmervisit-business.git -> business
https://github.com/arun-0/jaisalmervisit-site.git -> site
Never overwrite an existing directory or discard local changes.

Read business/CLAUDE.md, business/AGENTS.md,
business/dir-structure.md, business/TODO.md, the newest WORKLOG entry
and business/NEXT-PROMPT.md. Read site/AGENTS.md and site/README.md.
Ensure this local Claude Code session can work with both checkouts.
For later sessions, start in business with site as an allowed sibling.

Verify account, remotes, clean/preserved working-tree state and open
PRs in both repositories. Stop after this first bootstrap with the
actual paths, readiness/blockers and recommended next task.
Do not modify project content, commit, push, deploy or touch main yet.
```

### After setup — contributor turn

```text
I am the Jaisalmer Visit site owner, collaborating through GitHub
account jaisalmer-visit. arun-0 controls main in both repositories.

Read CLAUDE.md, AGENTS.md, dir-structure.md, TODO.md, the newest
WORKLOG entry and the contributor setup in setup/assistant-portability.md.
Read ../site/AGENTS.md and ../site/README.md before site work.

Confirm the local checkout paths and GitHub identity. Fetch both
repositories, preserve local work, and inspect open PRs/handovers.
Take the highest-value unblocked task that isn't already under review,
using the India-first strategy and existing approvals. Explain your
initial recommendation early, then carry useful independent work through.

Work on topic branches. Verify relevant changes, update the shared
TODO/WORKLOG/dashboard and commit using my configured human identity,
with no AI attribution. Push every changed repository and open PRs
against main; cross-link paired code/business PRs. Record the task ID,
checks, dependencies and exact next action. Prepared or PR-ready work
is not yet merged, deployed or earning revenue.

Never push or merge main, bypass its rules, change visibility/access,
or deploy independently. Private/legal account steps stay with the
actual payee; never commit IDs, credentials or customer data. Honour
recorded check-after conditions and don't repeat answered questions.
Stop with review-ready PR links and a concise handover for arun-0.
```

Model/subscription guidance checked 22 November 2026: [Pro includes Claude Code](https://support.claude.com/en/articles/11145838-use-claude-code-with-your-pro-max-or-ultra-plan), [current model selection](https://support.claude.com/en/articles/11940350-claude-code-model-configuration), [effort settings](https://code.claude.com/docs/en/model-config#adjust-effort-level). These are recommendations; actual account/tool access is checked in his session.
