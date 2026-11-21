# Jaisalmer Visit — growth & revenue roadmap

*Started 14 Nov 2026. Claude updates the status column as work gets done.*

## 1. Where the site stands (review of 14 Nov 2026)

**What's good — keep it**
- Looks premium, mobile-first, fast-feeling. Better than most Jaisalmer guide sites.
- Real, useful features: itineraries by trip type, map, audio guide, Tourist Mode, transport directory with ratings.
- Technical basics in place: page description, social share image, structured data (schema.org), robots.txt, sitemap, AdSense with ads.txt, cookie consent.
- Social accounts exist (Instagram, Facebook, YouTube) and are linked.

**What's holding revenue back — in order of impact**

| # | Problem | Why it matters |
|---|---|---|
| 1 | **The whole site is one web page.** Fort, havelis, Kuldhara, itineraries etc. are sections of the home page (`#map/fort`), and the sitemap lists only 2 URLs. | Google ranks *pages*, not sections. Someone searching "Kuldhara village history" or "Jaisalmer 2 day itinerary" can't land on you. Search traffic is the main source of AdSense money, so this is the #1 limit on revenue. |
| 2 | **Only one ad slot**, and all content sits on that one page. | AdSense pays per page view and per ad seen. One page = few page views per visitor. |
| 3 | **Very little text per place** (one line each). | Google rewards pages that fully answer a question (timings, tickets, how to reach, how long, tips). |
| 4 | **Test listings are public** ("Service provider ltd", "WorkNeed App"), and the BEST CHOICE strip repeats each listing twice. | Looks unfinished to tourists and to businesses you want to sign up. |
| 5 | **All 15 images have no description (alt text).** | Lost Google Images traffic; small accessibility issue. |
| 6 | **The directory earns nothing yet.** | It is probably your biggest money opportunity (see section 2). |

## 2. Where the money is (honest view)

| Revenue stream | Potential | Effort | When |
|---|---|---|---|
| **AdSense** | Grows with page views. Indian traffic pays low per view (roughly a few dollars or less per 1,000 page views; we'll measure *your* number). Needs tens of thousands of monthly visits to be meaningful. | Medium (content) | Now. Grows with section 3 work. |
| **Featured / paid directory listings** (desert camps, jeep safaris, taxis, guides, restaurants) | High. A camp or taxi gets bookings from you, so a monthly fee for top placement is easy to justify once you have traffic. | Low–medium | Once traffic is visible (roughly 3+ months). Start collecting free listings now. |
| **Booking leads / commission** (desert camp, safari, taxi enquiries sent to partners) | Highest per visitor. Desert camps typically pay agents a commission per booking. | Medium (WhatsApp handling) | After listings, when enquiries come in. |
| **Affiliate links** (hotels via Booking.com/Agoda, tours via GetYourGuide/Klook) | Medium; works well with "where to stay" and itinerary pages. | Low | With the new pages. |
| Sponsored posts / reels for local businesses | Medium once Instagram has an audience. | Low | After ~5–10k followers. |

**Bottom line:** AdSense is your first income, but probably not your biggest one. The plan is to build search traffic (which raises AdSense), use that traffic to sell directory placements and bookings, and use Instagram to bring both visitors and businesses.

## 3. The plan

### Phase 1 — Foundations (weeks 1–4)
| Task | Who | Status |
|---|---|---|
| Set up Claude: profile, Project, Gmail/Drive connectors (`setup/claude-account-setup.md`) | You | To do |
| Give Claude read access to **Google Search Console** and **Google Analytics** data (or share screenshots) so we know real traffic | You | To do |
| Find out how the site is edited | You | Done: the engineer has the code. Brief for them in `content/engineer-brief.md`; send it and get a time estimate |
| Remove test listings; fix duplicated BEST CHOICE strip; add image descriptions | Developer / Claude | To do |
| **Give every place, itinerary and activity its own page** with its own address (e.g. `/kuldhara`, `/itinerary/2-days`), and list them all in the sitemap | Developer / Claude | To do |
| Submit the new sitemap in Search Console | You | To do |

### Phase 2 — Content that ranks (months 1–3)
Claude writes; you check local facts; the pages go live.
- One full page per attraction (14 now): history, what to see, timings, tickets, how to reach, time needed, tips, nearby places, map.
- Planning pages people actually search for: best time to visit, Jaisalmer in 2/3 days, Sam vs Khuri dunes, desert camp guide and price ranges, how to reach Jaisalmer, Jaisalmer from Jodhpur/Jaipur, where to stay, what to eat, shopping, Jaisalmer in summer, Desert Festival.
- Hindi versions of the top pages. Many Indian tourists search in Hindi, and fewer sites compete there.
- 2–3 ad slots per long page, placed between sections (not cluttered).
- Goal: 40–60 strong pages in 3 months.

### Phase 3 — Social (started 14 Nov 2026)
Full plan and ready-to-paste bios / WhatsApp texts: `social/social-media-plan.md`. First two weeks of posts: `social/calendar-2026-11-week1-2.md`.
- **Instagram: worth it now.** Jaisalmer is extremely visual. 3 reels + 2 carousels a week, each pointing to a page on the site. Claude writes hooks, captions, hashtags and a weekly calendar; you or a local reel photographer shoot.
- **Facebook:** cross-post the same content through Meta Business Suite. Low effort, low priority.
- **YouTube:** reuse reels as Shorts.
- **WhatsApp Business:** set up now with greeting, away message and quick replies (Claude writes them). It becomes important once booking enquiries start.

### Phase 4 — Monetise the directory (month 3+)
- Reach out to camps, safari operators, taxis and guides: free basic listing now, paid "Featured" spot later. Claude drafts the pitch and a one-page rate card; you approve each message.
- Add an "Enquire on WhatsApp" button on camp/safari listings to route leads through you.
- Agree commission with 3–5 trusted camps before the peak season (Oct–Mar).

### Phase 5 — Automation (ongoing, as each piece is proven)
| Automate | How |
|---|---|
| Weekly Instagram/Facebook drafts | Scheduled Claude task every Monday → drafts in `social/`, you approve |
| Inbox triage | Gmail connector: Claude summarises enquiries and drafts replies |
| Monthly report | Claude compiles traffic, AdSense and listings numbers into `reports/` |
| New listing checks | Claude reviews new "Add Your Service" submissions for spam/test entries |

## 4. Numbers to track monthly
Search clicks & impressions (Search Console) · visitors & page views (Analytics) · AdSense earnings & page RPM · Instagram followers & reach · listings (free / paid) · booking enquiries.
