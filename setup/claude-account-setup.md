# Setting up your Claude account for Jaisalmer Visit

This is the original Claude setup reference. The current shared workflow, exact project paths, Sol model preference and task prompts are in setup/chatgpt-workflows.md. HANDOFF.md and WORKLOG.md hold the shared business state.

You have two places to use Claude. Use each for what it is good at:

| Where | Use it for |
|---|---|
| **Code tab** (this window, desktop app) | The real work: reviewing your site, writing page content, research, files, scheduled weekly tasks, browsing as you. Open it in the folder `Desktop\ai\scratch` so it reads `CLAUDE.md` and knows your business. |
| **Chat** (claude.ai, or the Chat tab / phone app) | Quick questions on the go: a caption, a reply to a customer, a translation. Use the Project below so it also knows your business. |

---

## Step 1 — Profile preferences (2 minutes)

claude.ai → click your name (bottom left) → **Settings** → **Profile**. Paste this into the box asking what Claude should know or consider about you:

```
I run jaisalmervisit.com, a mobile-first travel guide and local business directory for Jaisalmer, Rajasthan. I earn from Google AdSense today and want to grow traffic and revenue. I'm new to Claude and not a professional marketer — explain things simply, give me concrete next steps, and tell me honestly when an idea isn't worth the effort. I write in English and Hindi; reply in the language I use. When drafting posts or messages for tourists, keep facts accurate and flag anything (prices, timings) I should check locally.
```

Also in Settings, check that **memory** is on, so Chat remembers context between conversations.

## Step 2 — One Project for the business (5 minutes)

claude.ai → **Projects** → **Create project**. Name: `Jaisalmer Visit`.

**Project instructions** (paste this):

```
This project is for running jaisalmervisit.com — a travel guide to Jaisalmer with attractions, itineraries, things to do, a map, an audio guide and a directory of local businesses (desert camps, restaurants, guides, bike/car rental, autos). Revenue: Google AdSense now; directory listings, bookings and affiliate income are being explored. Audience: Indian domestic tourists first, foreign tourists second.

When I ask for content:
- Social posts: Instagram first (reels and carousels), short hooks, 5–10 relevant hashtags, a clear call to action pointing to jaisalmervisit.com.
- Website text: helpful, specific, written for someone planning a trip; include practical details (timings, distance, rough cost, best time) and mark anything to verify.
- Replies to tourists or businesses: warm, short, professional; never promise prices or availability I haven't confirmed.

Always end with the one next action I should take.
```

**Project knowledge** (upload files): start with `CLAUDE.md` and `strategy\roadmap.md` from the workspace folder. Add your price lists, listing rules and any partner agreements later.

You don't need more Projects yet. Make a second one only if a separate business comes along.

## Step 3 — Connectors

claude.ai → Settings → **Connectors**.

| Connector | Do it? | What it enables |
|---|---|---|
| **Gmail** | Yes | Claude can read and search your business inbox, summarise enquiries and draft replies. It drafts; you press send. |
| **Google Drive** | Yes | Claude can read your docs and sheets (listings sheet, price lists). |
| **Google Calendar** | Optional | Useful once you schedule calls with partner businesses. |
| Facebook / Instagram / WhatsApp | No official connector | See below. |

**Facebook, Instagram and WhatsApp:** Claude has no direct connector for these. The practical setup:
- **Instagram and Facebook:** Claude writes the posts and a weekly calendar. You (or Claude, through your Chrome browser with your approval for each post) schedule them in **Meta Business Suite**, which posts to both from one place.
- **WhatsApp:** install **WhatsApp Business** (free) on the business number. Set its greeting message, away message, quick replies and catalogue; Claude writes all of that text. Fully automatic replies need the paid WhatsApp Business API, which is worth it only once enquiries are many per day.

## Step 4 — What Claude will and won't do on your behalf

You've given Claude a free hand to think and plan, and it will. For safety, some things always come back to you:

- **Claude does freely:** research, plans, drafts of pages/posts/emails/replies, site reviews, reports, and weekly scheduled drafting tasks.
- **Claude asks you first, every time:** publishing a post, sending an email or message, contacting a business, changing AdSense / Google / Meta settings, spending money.
- **Claude never does:** type passwords, OTPs, bank or card details. You sign in yourself; Claude works in the browser after that.

This keeps one wrong click from costing you your AdSense account or your reputation, and it still saves you most of the work.

## Step 5 — Daily habit (once set up)

- Open the Code tab in this folder and say what you need. Claude already knows the business from `CLAUDE.md`.
- Each week Claude can prepare, automatically, the next week's Instagram posts and a list of enquiries to answer, ready for your approval. We'll set this up after the basics are working.
