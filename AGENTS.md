# Jaisalmer Visit — business workspace

Instructions for any AI assistant working in this folder (Claude Code reads it via `CLAUDE.md`; Codex/ChatGPT reads this file directly). Keep it short and current. **This is the single source of rules: edit here, not in `CLAUDE.md`.**

## The business
- **Site:** https://jaisalmervisit.com — a mobile-first travel guide to Jaisalmer, Rajasthan.
- **What it has today (Nov 2026):** attractions, itineraries (1–3 days, weekend, desert, heritage, family, couple), things to do, an interactive map, an audio guide, "Tourist Mode", a newsletter signup, and a **local business directory** (restaurants, desert camps, bike/car rental, guides, autos) where providers can "Add Your Service" after mobile verification.
- **Tech:** static site on Firebase Hosting; backend on Firebase (Firestore, Cloud Storage on the Blaze plan, Auth for phone verification), project `visitjaisalmer-e3085`. Built by an engineer (footer credits Parihar AI, pariharai.com). DNS on Cloudflare (DNS-only). Hosting move plan: `strategy/git-and-hosting-plan.md`.
- **Revenue today:** Google AdSense (publisher `pub-9028150722368329`, ads.txt in place, non-personalised ads).
- **Channels:** Instagram @jaisalmervisit_, Facebook page (id 61595294556976), YouTube @JaisalmerVisit.

## Goals (owner's words, paraphrased)
1. Maximise revenue — AdSense first, other streams when worth it.
2. Make the site popular (search traffic + social).
3. Use Facebook / Instagram / WhatsApp when it pays off.
4. Automate as much of the running of the business as possible with AI.

## How to work here
- The owner is new to AI tools and not a marketer by trade: explain in plain language, give concrete next steps, avoid jargon. The owner's elder brother is technical; with him, technical detail is fine.
- Think like an owner: rank ideas by revenue impact vs effort; say no to low-value work.
- Always draft first. **Posting, sending messages/emails, changing ad or account settings, spending money, or contacting listed businesses needs the owner's explicit yes each time.**
- Never ask for or type passwords, OTPs, bank or card details. People sign in themselves.
- Keep facts about places, prices and timings accurate; flag anything that needs checking locally.

## Two people share this folder
The owner and the owner's elder brother both work here, on different computers and possibly different AI tools, taking turns.
- **At the start of a session:** read the top entry of `WORKLOG.md` and tell the person what changed since they last worked.
- **At the end of a session** (or when the person says they're done): add an entry to the top of `WORKLOG.md` (date, who, done, waiting on, next) and give them a one-line WhatsApp message they can send ("Done: … Next for you: …").
- An AI tool's own memory belongs to one person and one computer, so anything both people need goes in this folder, never only in memory.

## Folder map
- `WORKLOG.md` — who did what, newest first. The handover between the two people.
- `HANDOFF.md` — orientation for someone new to this work.
- `setup/` — how the owner's Claude account is set up (profile text, Project instructions, connectors).
- `strategy/` — site audit, growth/revenue roadmap, Git and hosting plan. `strategy/roadmap.md` is the master plan; update its status as work is done.
- `content/` — drafts for new site pages and blog posts, and the engineer brief.
- `social/` — Instagram / Facebook / WhatsApp drafts and calendars.
- `reports/` — monthly numbers (traffic, AdSense, listings) once the owner shares them.
