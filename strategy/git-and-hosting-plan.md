# Git, source code and hosting plan

*20 Nov 2026. Written for the brother driving the technical work.*

## What the live site actually runs on (checked 20 Nov 2026)
- **Static hosting:** Firebase Hosting (Fastly `x-served-by` headers, `/__/firebase/init.json` responds). Cloudflare is the DNS provider but is **not proxying** (no `cf-*` headers), so the records are DNS-only and point at Firebase.
- **Backend (stays on Firebase regardless of where hosting goes):**
  - Firestore: listings, reviews, announcements.
  - Cloud Storage: admin image/audio uploads. Needs the **Blaze (pay-as-you-go) plan**, so a billing account is attached. Probably the engineer's.
  - Firebase Auth: provider "Add Your Service" phone verification. `authDomain` is `visitjaisalmer-e3085.firebaseapp.com`, so auth does **not** depend on where the HTML is hosted.
  - An admin panel under `/admin`.
- Firebase web API key is restricted to the site's domains, so any new preview domain must be added to its allowed referrers.
- No Cloud Functions calls seen from the front end. Confirm in the repo (`functions/` folder).

**Consequence:** the real lock-in is the **Firebase project and its billing account**, not the hosting. Fixing ownership comes before anything else.

---

## Step 0 — Ownership first (owner + engineer, ~1 day)
| Account | Action |
|---|---|
| **Firebase / Google Cloud project `visitjaisalmer-e3085`** | Engineer adds the owner's Google account as **Owner** (Google Cloud console → IAM). Then move billing to the owner's own billing account and set a **budget alert** (e.g. ₹1,000/month). Engineer can stay as Editor while still working on it. |
| **GitHub** | Create a free **GitHub organisation** (e.g. `jaisalmervisit`) **owned by the owner's GitHub account** (create one with the business Gmail). Brother = admin member. Engineer = collaborator on the site repo only. |
| **Cloudflare** | Don't share the owner's login. Owner invites the brother: Manage Account → Members, role limited to DNS + Pages (or Administrator, temporarily). Remove or reduce when done. |
| **Everything** | 2-step verification on, owner's email as account owner: domain registrar, Cloudflare, Google (AdSense, Analytics, Search Console, Firebase), GitHub, Meta. |
| **Engineer agreement** | Short written note: code and data belong to the owner. The handover must include everything: `firebase.json`, `.firebaserc`, `firestore.rules`, `storage.rules`, indexes, admin panel, any `functions/`, build scripts, and **git history** if they have it. |

## Step 1 — Git on this laptop
- Install Git for Windows and GitHub CLI: `winget install Git.Git GitHub.cli`.
- `gh auth login` (the brother signs in himself in the browser; Claude never needs the password).
- Move the workspace out of the folder named `scratch` to something permanent before `git init`, e.g. `Desktop\jaisalmervisit\business` and `Desktop\jaisalmervisit\site`.

## Step 2 — Repo 1: `business` (private): shared work
- Contents: today's workspace (`CLAUDE.md`, `WORKLOG.md`, `strategy/`, `social/`, `content/`, `setup/`, `HANDOFF.md`).
- Workflow: pull → work → Claude updates `WORKLOG.md` → commit + push → WhatsApp "done". The other person's Claude runs `git pull` and summarises `git log`/diff since their last session.
- Owner doesn't need to learn Git: in either Claude session, say "get latest" / "save and share my work" and Claude runs pull / commit / push.
- Commit straight to `main`; two people taking turns don't need branches here.
- Add a rule to `CLAUDE.md`: pull at start, commit + push at end.

## Step 3 — Repo 2: `site` (private): website source
- Best: engineer pushes their **full git history** into the new repo. Fallback: import the zip as the first commit ("Import from engineer, <date>").
- Before the first commit: check for secrets (service-account JSON, `.env`, private keys) and add a `.gitignore` (`node_modules/`, `.firebase/`, `*.log`, `.env*`, service-account files). The Firebase web config is public by design; service-account keys are not.
- Add a `README.md`: how to run locally (it already supports the Firebase emulators), how to build, how to deploy.
- Branch rule: `main` = what's live; changes go via a branch + pull request, so the owner (or Claude) can review and Cloudflare builds a preview URL first.
- Keep it **separate from `business`**: different people (the engineer shouldn't see business strategy), different history, deploys on its own.

## Step 4 — Hosting: move the static site to Cloudflare Pages (optional, recommended *after* Steps 0–3)
**Why move:** deploys on every push to `main` with no Firebase login, a free preview URL per pull request, free, and it's where the DNS already is. It also suits the planned SEO rebuild (pre-rendered page per place).
**Why it's safe:** only the HTML/JS/CSS moves. Firestore, Storage and Auth stay on Firebase unchanged.

1. Build the site locally from the repo and confirm it matches production.
2. Port `firebase.json` hosting config (redirects, rewrites, headers, clean URLs, `/admin`) to Pages `_redirects` / `_headers`. Check whether the code reads `/__/firebase/init.json` (Firebase-only URL); if so, switch it to the inline config.
3. Create the Pages project connected to the `site` repo. Deploy to `*.pages.dev`.
4. For the preview domain to work, add `*.pages.dev` (or the specific project domain) to the **API key's HTTP referrer list** (Google Cloud console → Credentials), and to **Firebase Auth → Authorized domains** if phone verification is tested there.
5. Test on the preview: listings load, reviews, map, audio guide, Add Your Service (phone OTP), admin login and uploads, `ads.txt`, `robots.txt`, `sitemap.xml`, AdSense script loads.
6. **Before switching:** export the current DNS records in Cloudflare (screenshot or export) so rollback is one edit.
7. Pages → Custom domains → add `jaisalmervisit.com` and `www`. Cloudflare rewrites the DNS records itself.
   **No nameserver change is needed:** nameservers already point to Cloudflare.
8. Watch for 48 hours: site, AdSense, Analytics, Search Console. Rollback = restore the old DNS records. Keep Firebase Hosting deployed (untouched) for a month as the fallback.
9. Later, optionally turn on Cloudflare proxy features (caching, analytics). Test AdSense after any change.

## Order and rough effort
| # | Step | Who | Effort |
|---|---|---|---|
| 0 | Ownership: Firebase owner + billing, GitHub org, Cloudflare member | Owner + engineer | 1 day (mostly waiting on engineer) |
| 1 | Git + gh on laptop, move folders | Brother + Claude | 30 min |
| 2 | `business` repo | Claude | 15 min |
| 3 | `site` repo with history, secrets check, README | Brother + Claude | 1–2 h |
| 4 | Cloudflare Pages move | Brother + Claude | Half a day + 48 h watch |
| 5 | Then the SEO rebuild from `content/engineer-brief.md` | Brother/engineer + Claude | Ongoing |

**Don't combine the hosting move and the SEO rebuild in one change.** Move first with zero changes, confirm nothing broke, then start the SEO work.
