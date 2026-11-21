# Handoff — Jaisalmer Visit growth work

*Updated 20 Nov 2026. For the owner's elder brother, who is taking this work over end to end.*

## 1. What this is
In November 2026 the owner of **jaisalmervisit.com** (a Jaisalmer travel guide + local business directory, earning from Google AdSense) started working with Claude (Claude Code, desktop app) to grow traffic and revenue and to automate the business. This bundle is **everything from that first session**: the plans, ready-to-use content, the rules the AI follows, and the full conversation transcript.

Nothing has been changed on the live website, the ad account or the social accounts yet. Everything here is plans and drafts.

## 2. What's in the bundle
| Path | What it is | Read it when |
|---|---|---|
| `HANDOFF.md` | This guide | First |
| `AGENTS.md` | **The rules any AI tool follows in this folder**: business facts, goals, approval rules, two-person routine. Codex reads it automatically. | Second |
| `CLAUDE.md` | One line that makes Claude read `AGENTS.md`. Don't edit; edit `AGENTS.md`. | — |
| `WORKLOG.md` | Who did what, newest first. Your handover with the owner. | Every session |
| `strategy/roadmap.md` | **Master plan**: site review, revenue options, 5 phases, status | Third |
| `strategy/git-and-hosting-plan.md` | **Technical plan**: ownership of Firebase/GitHub/Cloudflare, two repos, optional move to Cloudflare Pages | Before any technical work |
| `content/engineer-brief.md` | SEO changes for the site (one URL per place, sitemap, ad slots, quick fixes) | Before touching site code |
| `social/social-media-plan.md` | Social strategy + ready-to-paste bios and WhatsApp Business texts | Before social work |
| `social/calendar-2026-11-week1-2.md` | 10 ready posts (16–29 Nov 2026). Dates have passed; reuse the posts with new dates | Before social work |
| `setup/claude-account-setup.md` | How the owner sets up claude.ai (profile, Project, connectors) | If you use Claude |
| `claude-memory/` | Facts Claude saved to its own memory on the owner's laptop | Reference only |
| `session-transcript/session-export.zip` | Full export of the Claude session (conversation, tool calls, metadata), up to the moment the bundle was built | When you need the "why" behind a decision |

**Reading the transcript:** unzip `session-transcript/session-export.zip`. The conversation is stored as JSON lines (`.jsonl`), which are hard to read by eye. Ask your AI tool: *"Summarise the conversation in session-transcript/ — decisions made, open questions, and anything not captured in the other files."* The transcript also contains the owner's account details and everything discussed, so keep it private.

## 3. Key findings so far (short version)
1. **The site is one page to Google** (all places are `#sections`; sitemap lists 2 URLs). This caps search traffic and AdSense income. Fix = one real URL per place (`content/engineer-brief.md`).
2. **The business directory is the bigger money opportunity** (featured listings, desert-camp booking commission), more than AdSense.
3. **Social is almost empty** (Instagram 7 followers / 2 posts, YouTube 1 Short). Instagram is the main channel to build; the plan and posts are ready.
4. **Ownership risk:** the Firebase project (database, uploads, phone auth, billing) is controlled by the engineer. Getting the owner made Owner is the first technical step.

## 4. How to take over — step by step

### Step 1 — Get set up (≈1 hour)
1. Unzip this bundle into a permanent folder: `Documents\jaisalmervisit\business` (the engineer's code goes next to it in `site\`; see Step 1b).
2. Open the folder in your AI tool, using **your own account** (not the owner's):
   - **Codex / ChatGPT:** open the folder; it reads `AGENTS.md` automatically.
   - **Claude Code:** desktop app → Code tab → choose the folder; it reads `CLAUDE.md` → `AGENTS.md`.
3. First message:
   > Read HANDOFF.md, AGENTS.md, WORKLOG.md, strategy/roadmap.md and strategy/git-and-hosting-plan.md. Then summarise the transcript in session-transcript/. Tell me where things stand and what I should do first.
4. Ask the owner for the accesses in section 5. **Invitations only, no passwords.**

### Step 1b — Where the engineer's source code goes
Keep the website code **next to** this bundle, not inside it. They become two separate Git repos (`business` and `site`), so the engineer can be given the code without seeing business plans.

```
Documents\jaisalmervisit\
├── business\   ← this bundle (HANDOFF.md, AGENTS.md, strategy\, social\ …)
└── site\       ← unzip the engineer's code here (the folder that contains firebase.json)
```

1. Unzip the engineer's zip into `Documents\jaisalmervisit\site`. Make sure `firebase.json` / `package.json` sit directly in `site\`, not in an extra subfolder.
2. **Don't run `firebase deploy` or change anything live yet.** You don't have access to the Firebase project, and the owner needs to own it first.
3. Open `site\` in your AI tool (Codex or Claude Code: a separate session from `business\`) and paste the prompt below. Its job is to understand and document the code, not to change the site.

**First prompt for the `site` folder (works in Claude Code and Codex):**
```
This folder is the source code of https://jaisalmervisit.com, handed over by the
original engineer as a zip. The business context and plans are in ../business
(read ../business/AGENTS.md, ../business/strategy/git-and-hosting-plan.md and
../business/content/engineer-brief.md first).

Do NOT deploy, publish, or change anything live, and do not run firebase deploy.
Read-only analysis and local files only.

1. Map the project: framework/build setup, folder structure, where places,
   itineraries and listings data live, the admin panel, Firebase usage
   (Firestore, Storage, Auth, any Cloud Functions), firebase.json hosting config
   (rewrites, redirects, headers), firestore.rules and storage.rules.
2. Check for secrets that must not go into Git (service-account JSON, .env files,
   private keys, tokens). List them; don't print their values.
3. Check whether this code matches the live site (compare asset file names and
   page content with https://jaisalmervisit.com). Flag anything missing from the zip.
4. Write: README.md (how to run locally with the Firebase emulators, build,
   deploy), a .gitignore, and an AGENTS.md for this repo (what the site is,
   rules: no deploys without the owner's approval, no secrets in Git,
   main = live).
5. Tell me: what is needed to (a) put this in a private GitHub repo,
   (b) host the static site on Cloudflare Pages while keeping Firebase as the
   backend, and (c) build one real URL per place for SEO, with risks and an
   effort estimate for each.
```

After that, follow Step 2 to turn both folders into GitHub repos.

### Step 2 — Ownership and Git (week 1)
Follow `strategy/git-and-hosting-plan.md`, Steps 0–3:
1. **Ownership:** engineer adds the owner's Google account as **Owner** of Firebase project `visitjaisalmer-e3085` and moves billing to the owner. Set a budget alert.
2. **GitHub:** create an organisation **owned by the owner's GitHub account** (you as admin). Create two private repos:
   - `business`: push this folder. From then on, both of you pull → work → update `WORKLOG.md` → commit → push → WhatsApp "done". The owner just tells their AI "get latest" / "save and share my work".
   - `site`: the engineer's code. Ask the engineer for full git history; otherwise import the zip you have. Scan for secrets and add `.gitignore` before the first commit.
3. On the owner's laptop: install Git + GitHub CLI and clone `business` there (the owner deferred this; do it together).

### Step 3 — Quick wins while ownership is sorted (week 1–2)
- Social: paste the bios, set up WhatsApp Business texts and Google Business Profile, start posting from the calendar (`social/`). The owner approves each post.
- Send `content/engineer-brief.md` to the engineer (or do it yourself once the `site` repo exists).
- Get numbers: Search Console, Analytics and AdSense access (section 5) → first monthly report in `reports/`.

### Step 4 — Hosting move (optional, after Steps 2–3 are solid)
`strategy/git-and-hosting-plan.md` Step 4: Cloudflare Pages for the static site, Firebase stays for the backend. **Nameservers don't change** (already Cloudflare); only DNS records change, and rollback = restore them. Don't combine with SEO changes.

### Step 5 — Growth work (ongoing)
`strategy/roadmap.md` Phases 2–5: page per place + Hindi pages, directory monetisation (featured listings, camp commission), automation (weekly social drafts, inbox triage, monthly report).

### Every session
Start: pull, read the top of `WORKLOG.md`. End: AI writes a `WORKLOG.md` entry + a one-line WhatsApp message; commit + push; send it to the owner.

## 5. Accesses the owner needs to give
**Rule: never share passwords or OTPs, with the brother or with any AI tool.** Every service below has an "invite a person" feature. The owner stays the owner; access is removed when no longer needed.

| Service | What the brother needs | How the owner grants it | When |
|---|---|---|---|
| **Cloudflare** (DNS, future hosting) | Member: DNS + Pages (or Administrator temporarily) | Cloudflare → Manage Account → Members → Invite | Before hosting work |
| **GitHub** | Admin of the organisation | Owner creates the org, invites the brother | Week 1 |
| **Firebase / Google Cloud** `visitjaisalmer-e3085` | Editor (or Firebase Admin) | Only after the engineer makes the owner Owner: Google Cloud console → IAM → Grant access | Week 1–2 |
| **Google Search Console** | Full user | Search Console → Settings → Users and permissions | Week 1 |
| **Google Analytics** | Viewer (Editor if changing tracking) | Analytics → Admin → Property access management | Week 1 |
| **Google AdSense** | Standard user (to see earnings) | AdSense → Account → Access and authorisation → User management | Week 1 |
| **Meta (Facebook page + Instagram)** | Partial access to page + Instagram account, for scheduling posts | Meta Business Suite → Settings → People → Add | When social work starts |
| **YouTube** | Manager | YouTube Studio → Settings → Permissions → Invite | When social work starts |
| **Engineer's code** | Already with the brother | — | Done |
| **Domain registrar** | Nothing (nameservers already on Cloudflare) | — | — |
| **Business Gmail** | Usually nothing. If needed: Gmail → Settings → Accounts → "Grant access to your account" (delegation, no password) | Optional | Only if handling enquiries |
| **WhatsApp Business** | Nothing for now; it stays on the owner's phone | — | Revisit when enquiries grow |
| **AI tool** | His own ChatGPT/Codex or Claude account, not the owner's | — | Now |

## 6. Ground rules (also in `AGENTS.md`)
- AI drafts; a human approves every post, message, email, settings change or payment.
- No passwords/OTPs in any AI chat, file or repo.
- Owner keeps ownership of every account; others are invited members.
- Anything both people need goes in this folder, not in one person's AI memory.
